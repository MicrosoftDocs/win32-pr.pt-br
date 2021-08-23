---
title: Protegendo arquivos com DRM versão 1
description: Protegendo arquivos com DRM versão 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows SDK de Formato de Mídia, criando arquivos protegidos
- Windows SDK de Formato de Mídia, arquivos protegidos
- ASF (Advanced Systems Format), criando arquivos protegidos
- ASF (Formato de Sistemas Avançados), criando arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (Formato de Sistemas Avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM.lib
- ASF (Formato de Sistemas Avançados),WMStubDRM.lib
- WMStubDRM.lib, criando arquivos protegidos
- WMStubDRM.lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM.lib
- DRM (gerenciamento de direitos digitais), WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b500f3711b8c92324cbd87d4dc199a8a0bb803cba69357a23f139fb96f8281f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084533"
---
# <a name="protecting-files-with-drm-version-1"></a>Protegendo arquivos com DRM versão 1

Quando esse tipo de proteção é aplicado, uma licença DRM versão 1 é gerada que é válida somente no computador do qual a solicitação de licença foi feita. Como nenhuma chave ou semente de chave está definida, não há como gerar licenças portáteis para conteúdo protegido usando essa técnica. No entanto, ao usar Windows SDK de Formato de Mídia 7.1 ou posterior, as licenças podem ser recuperadas no serviço de Migração de Licença da Microsoft.

Para proteger arquivos ASF usando DRM versão 1, execute as seguintes etapas:

1.  Vincule o arquivo WMStubDRM.lib ao seu projeto e, se necessário, desvincule wmvcore.lib.
2.  Chame a [**função WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para criar o autor. O primeiro argumento é reservado e deve ser definido como **NULL.**
3.  De definir um perfil para o autor a ser usado chamando [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Você deve definir um perfil no autor antes de definir os atributos drm. O DRM só tem suporte para perfis que usam os codecs Windows Media Audio ou Windows Media Video.
4.  Usando o [**método IWMHeaderInfo::SetAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) de definir as seguintes propriedades drm. A **propriedade \_ Usar DRM** instrui os componentes do DRM a proteger o conteúdo usando DRM versão 1. A **propriedade \_ Sinalizadores drm** especifica os direitos a serem incluídos na licença local que será criada para o conteúdo. O **valor LEVEL \_ do DRM** também é armazenado na licença; ele especifica o nível mínimo necessário para acessar o conteúdo. 150 é o nível recomendado para o conteúdo do DRM versão 1.

    | Atributo      | Valor                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Usar \_ DRM**   | **TRUE**                                                                                    |
    | **Sinalizadores DRM \_** | WMT \_ RIGHT \_ PLAYBACK \| WMT \_ RIGHT \_ COPY \_ TO \_ NON \_ SDMI \_ DEVICE \| WMT \_ RIGHT \_ COPY \_ TO \_ CD |
    | **NÍVEL DE \_ DRM** | 150                                                                                         |

    

     

O código de exemplo a seguir mostra como criar um autor habilitado para DRM para DRM versão 1 e definir as propriedades do DRM. A verificação de erro foi omitida para esclarecer.


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



 

 




