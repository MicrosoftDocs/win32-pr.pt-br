---
title: Especificando as ações a serem executadas
description: Especificando as ações a serem executadas
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- ASF (Advanced Systems Format), especificando ações
- ASF (formato de sistemas avançados), especificando ações
- DRM (gerenciamento de direitos digitais), especificando ações
- DRM (gerenciamento de direitos digitais), especificando ações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365597"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="732c2-107">Especificando as ações a serem executadas</span><span class="sxs-lookup"><span data-stu-id="732c2-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="732c2-108">Quando você chama o [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) pela primeira vez para criar o objeto de leitor, o segundo parâmetro é um valor de bit que é **ou** de [**\_ direitos de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="732c2-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="732c2-109">Use esse parâmetro para especificar quais ações o aplicativo executará no primeiro arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="732c2-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="732c2-110">Essas ações correspondem diretamente aos direitos que podem ser especificados na licença.</span><span class="sxs-lookup"><span data-stu-id="732c2-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="732c2-111">Nas chamadas subsequentes para [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), você pode modificar os direitos que você está solicitando chamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), especificando a constante definida para a propriedade [**\_ direitos de DRM**](drm-rights.md) e usando literais de cadeia de caracteres (do tipo **WCHAR**) separados por ponto e vírgula para identificar os direitos.</span><span class="sxs-lookup"><span data-stu-id="732c2-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="732c2-112">O trecho de código a seguir solicita quatro direitos: executar o arquivo, copiá-lo para um dispositivo e reproduzi-lo como parte de uma lista de reprodução colaborativa.</span><span class="sxs-lookup"><span data-stu-id="732c2-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="732c2-113">Não confunda a [**propriedade \_ direitos de DRM**](drm-rights.md) com a propriedade de [**\_ sinalizadores DRM**](drm-flags.md) , que é uma **DWORD** usada para especificar quais direitos aplicar a uma licença local do DRM versão 1 ao copiar o conteúdo de um CD.</span><span class="sxs-lookup"><span data-stu-id="732c2-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="732c2-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="732c2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="732c2-115">**Lendo arquivos protegidos**</span><span class="sxs-lookup"><span data-stu-id="732c2-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




