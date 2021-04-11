---
title: Protegendo arquivos com DRM versão 1
description: Protegendo arquivos com DRM versão 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- SDK do Windows Media Format, criando arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), criando arquivos protegidos
- ASF (formato de sistemas avançados), criando arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, criando arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104293853"
---
# <a name="protecting-files-with-drm-version-1"></a>Protegendo arquivos com DRM versão 1

Quando esse tipo de proteção é aplicado, é gerada uma licença do DRM versão 1 que é válida somente no computador do qual a solicitação de licença foi feita. Como nenhuma semente de chave ou chave está definida, não há como gerar licenças portáteis para conteúdo protegido usando essa técnica. No entanto, ao usar o Windows Media Format SDK 7,1 ou posterior, as licenças são recuperáveis no serviço de migração de licença da Microsoft.

Para proteger os arquivos ASF usando o DRM versão 1, execute as seguintes etapas:

1.  Vincule o arquivo WMStubDRM. lib ao seu projeto e, se necessário, desvincule o WMVCORE. lib.
2.  Chame a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para criar o gravador. O primeiro argumento é reservado e deve ser definido como **nulo**.
3.  Defina um perfil para o gravador a ser usado chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Você deve definir um perfil no gravador antes de definir qualquer atributo DRM. Somente há suporte para DRM para perfis que usam os codecs de vídeo do Windows Media Audio ou Windows Media.
4.  Usando o método [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , defina as seguintes propriedades de DRM. A propriedade **usar \_ DRM** INSTRUI os componentes DRM para proteger o conteúdo usando o DRM versão 1. A propriedade de **\_ sinalizadores DRM** especifica os direitos a serem incluídos na licença local que será criada para o conteúdo. O valor de **\_ nível de DRM** também é armazenado na licença; ele especifica o nível mínimo necessário para acessar o conteúdo. 150 é o nível recomendado para conteúdo DRM versão 1.

    | Atributo      | Valor                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Usar \_ DRM**   | **TRUE**                                                                                    |
    | **Sinalizadores de DRM \_** | WMT \_ de \_ reprodução \| direita \_ WMT \_ copiar \_ para \_ \_ dispositivo não \_ SDMI \| WMT \_ copiar à direita \_ \_ para \_ CD |
    | **nível de DRM \_** | 150                                                                                         |

    

     

O código de exemplo a seguir mostra como criar um gravador habilitado para DRM para DRM versão 1 e definir as propriedades de DRM. A verificação de erros foi omitida por questão de Clarify.


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




