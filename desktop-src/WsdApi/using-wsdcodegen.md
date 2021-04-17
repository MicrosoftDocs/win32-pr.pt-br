---
description: Descreve o processo de criação de um aplicativo WSDAPI usando o WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Usando WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763337"
---
# <a name="using-wsdcodegen"></a><span data-ttu-id="890a5-103">Usando WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="890a5-103">Using WsdCodeGen</span></span>

<span data-ttu-id="890a5-104">**Para compilar um aplicativo WSDAPI usando WsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="890a5-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="890a5-105">Defina o contrato funcional para o host do dispositivo em um arquivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="890a5-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="890a5-106">Gere um arquivo de configuração usando WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="890a5-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="890a5-107">Para obter mais informações, consulte [arquivo de configuração WsdCodeGen](wsdcodegen-configuration-file.md) e [sintaxe de linha de comando WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="890a5-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="890a5-108">Abra o arquivo de configuração gerado e modifique o arquivo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="890a5-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="890a5-109">Se você estiver criando um aplicativo cliente, pouca ou nenhuma modificação será necessária.</span><span class="sxs-lookup"><span data-stu-id="890a5-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="890a5-110">Se você estiver criando um aplicativo host, altere os elementos de configuração específicos do usuário (como [**manufacturer**](manufacturer.md) e [**ModelName**](modelname.md)).</span><span class="sxs-lookup"><span data-stu-id="890a5-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="890a5-111">Gere código usando WsdCodeGen, fornecendo o arquivo de configuração como entrada.</span><span class="sxs-lookup"><span data-stu-id="890a5-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="890a5-112">Para obter mais informações, consulte [sintaxe de linha de comando WsdCodeGen](wsdcodegen-command-line-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="890a5-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="890a5-113">Use o código gerado para criar um cliente, host ou ambos.</span><span class="sxs-lookup"><span data-stu-id="890a5-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="890a5-114">O SDK do Windows inclui alguns arquivos WSDL de exemplo, arquivos de configuração WsdCodeGen e código gerado.</span><span class="sxs-lookup"><span data-stu-id="890a5-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="890a5-115">Para obter mais informações, consulte [exemplos de WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="890a5-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="890a5-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="890a5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="890a5-117">Exemplos de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="890a5-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



