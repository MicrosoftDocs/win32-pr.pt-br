---
description: O serviço de detecção de script ELS é chamado de detecção de script da Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Detecção de script da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090952"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="93ba8-103">Detecção de script da Microsoft</span><span class="sxs-lookup"><span data-stu-id="93ba8-103">Microsoft Script Detection</span></span>

<span data-ttu-id="93ba8-104">O serviço de detecção de script ELS é chamado de detecção de script da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93ba8-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="93ba8-105">Esse serviço permite que os aplicativos detectem os scripts em que o texto é gravado.</span><span class="sxs-lookup"><span data-stu-id="93ba8-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="93ba8-106">O equivalente do NLS (suporte ao idioma nacional) de um serviço de detecção de script é a função [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) .</span><span class="sxs-lookup"><span data-stu-id="93ba8-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="93ba8-107">No entanto, o serviço ELS também recupera os intervalos de texto que pertencem a cada sistema de escrita.</span><span class="sxs-lookup"><span data-stu-id="93ba8-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="93ba8-108">Entrada para a detecção de script da Microsoft</span><span class="sxs-lookup"><span data-stu-id="93ba8-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="93ba8-109">A entrada para o serviço de detecção de scripts da Microsoft é o texto UTF-16 para o qual o serviço determina os intervalos de script.</span><span class="sxs-lookup"><span data-stu-id="93ba8-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="93ba8-110">Saída da detecção de script da Microsoft</span><span class="sxs-lookup"><span data-stu-id="93ba8-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="93ba8-111">A saída do serviço de detecção de scripts da Microsoft é uma matriz de intervalos, cada um contendo uma cadeia de caracteres UTF-16 terminada em nulo com o nome especificado Unicode do sistema de gravação associado.</span><span class="sxs-lookup"><span data-stu-id="93ba8-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="93ba8-112">O serviço relata os caracteres normais comuns (Zyyy) e herdados (Qaai) como pertencentes ao intervalo de script anterior.</span><span class="sxs-lookup"><span data-stu-id="93ba8-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="93ba8-113">O início de caracteres comuns e herdados é relatado como pertencente ao próximo intervalo de script.</span><span class="sxs-lookup"><span data-stu-id="93ba8-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="93ba8-114">Se todos os caracteres no texto de entrada forem comuns ou herdados, a saída do serviço será um intervalo único com a cadeia de caracteres vazia como seus dados.</span><span class="sxs-lookup"><span data-stu-id="93ba8-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="93ba8-115">Operação de detecção de script da Microsoft</span><span class="sxs-lookup"><span data-stu-id="93ba8-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="93ba8-116">O serviço de detecção de scripts da Microsoft mapeia os pontos de código pertencentes ao intervalo comum para o sistema de escrita anterior.</span><span class="sxs-lookup"><span data-stu-id="93ba8-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="93ba8-117">Como alternativa, o serviço pode mapear os pontos de código para o próximo sistema de escrita se os pontos de código estiverem no início da cadeia de caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="93ba8-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="93ba8-118">O aplicativo não precisa lidar com o intervalo comum.</span><span class="sxs-lookup"><span data-stu-id="93ba8-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="93ba8-119">GUID de detecção de script da Microsoft</span><span class="sxs-lookup"><span data-stu-id="93ba8-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="93ba8-120">O GUID para o serviço Microsoft Detecção de Idioma é declarado em Elssrvc. h, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="93ba8-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="93ba8-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93ba8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93ba8-122">Sobre os serviços lingüísticos estendidos</span><span class="sxs-lookup"><span data-stu-id="93ba8-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



