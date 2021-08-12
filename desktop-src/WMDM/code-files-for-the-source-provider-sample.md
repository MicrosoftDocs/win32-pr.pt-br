---
title: Arquivos de código para o exemplo do provedor de origem
description: Arquivos de código para o exemplo do provedor de origem
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Mídia Gerenciador de Dispositivos, exemplos
- Gerenciador de Dispositivos,exemplos
- Windows Mídia Gerenciador de Dispositivos, exemplo de provedor de serviços
- Gerenciador de Dispositivos, exemplo de provedor de serviços
- provedores de serviços, exemplos
- exemplos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c29127aebea6898868b29adb17a15c8d174e1fedfd3228bd565bf8ef4ce9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586363"
---
# <a name="code-files-for-the-source-provider-sample"></a>Arquivos de código para o exemplo do provedor de origem

O projeto do provedor de origem de exemplo inclui os seguintes arquivos de código-fonte, com os headers associados:



| Arquivo                   | Descrição                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch.cpp            | Inclui arquivos ATL padrão.                                                                                                                                                                                    |
| key.c                  | Contém uma chave de autenticação fi digital.                                                                                                                                                                            |
| loghelp.cpp            | Contém funções que registram a atividade e erros usando a **classe WMDMLogger,** que é implementada no arquivo WMDMLOG.dll sistema.                                                                         |
| MDServiceProvider.cpp  | Implementa uma classe, CMDServiceProvider, que implementa as interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.                                                             |
| mdsp.cpp               | Ponto de entrada de DLL e código de registro.                                                                                                                                                                          |
| MDSPDevice.cpp         | Implementa uma classe, CMDSPDevice, que implementa as interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages.**                          |
| MDSPEnumDevice.cpp     | Implementa uma classe, CMDSPEnumDevice, que implementa a interface [**IMDSPEnumDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)                                                                                                  |
| MDSPEnumStorage.cpp    | Implementa uma classe, CMDSPEnumStorage, que implementa a interface [**IMDSPEnumStorage.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)                                                                                               |
| MDSPStorage.cpp        | Implementa uma classe, CMDSPStorage, que implementa as interfaces [**IMDSPStorage2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2) [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                    |
| MDSPStorageGlobals.cpp | Implementa uma classe, CMDSPStorageGlobals, que implementa a interface [**IMDSPStorageGlobals.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)                                                                                      |
| MDSPutil.cpp           | Contém várias funções de utilitário para gerenciamento de dispositivos e arquivos.                                                                                                                                              |
| proppage.cpp           | Implementa uma classe, CPropPage, que herda as classes ATL **IPropertyPageImpl** (para implementar IPropertyPage) e **CDialogImpl,** que herda a classe ATL CDialogImpl (para gerenciar janelas e mensagens). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Provedor de Serviços de Exemplo**](sample-service-provider.md)
</dt> </dl>

 

 




