---
title: Arquivos de código para o exemplo de provedor de origem
description: Arquivos de código para o exemplo de provedor de origem
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de provedor de serviço
- Gerenciador de Dispositivos, exemplo de provedor de serviço
- provedores de serviços, exemplos
- exemplos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084085"
---
# <a name="code-files-for-the-source-provider-sample"></a>Arquivos de código para o exemplo de provedor de origem

O projeto de provedor de origem de exemplo inclui os seguintes arquivos de código-fonte, com cabeçalhos associados:



| Arquivo                   | Descrição                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch. cpp            | Inclui arquivos ATL padrão.                                                                                                                                                                                    |
| chave. c                  | Contém uma chave de autenticação fictícia.                                                                                                                                                                            |
| loghelp. cpp            | Contém funções que registram a atividade e os erros usando a classe **WMDMLogger** , que é implementada no arquivo do sistema WMDMLOG.dll.                                                                         |
| MDServiceProvider. cpp  | Implementa uma classe, CMDServiceProvider, que implementa as interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.                                                             |
| MDSP. cpp               | Ponto de entrada de DLL e código de registro.                                                                                                                                                                          |
| MDSPDevice. cpp         | Implementa uma classe, CMDSPDevice, que implementa as interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages** .                          |
| MDSPEnumDevice. cpp     | Implementa uma classe, CMDSPEnumDevice, que implementa a interface [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .                                                                                                  |
| MDSPEnumStorage. cpp    | Implementa uma classe, CMDSPEnumStorage, que implementa a interface [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .                                                                                               |
| MDSPStorage. cpp        | Implementa uma classe, CMDSPStorage, que implementa as interfaces [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .                    |
| MDSPStorageGlobals. cpp | Implementa uma classe, CMDSPStorageGlobals, que implementa a interface [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .                                                                                      |
| MDSPutil. cpp           | Contém várias funções de utilitário para gerenciamento de dispositivos e arquivos.                                                                                                                                              |
| PropPage. cpp           | Implementa uma classe, CPropPage, que herda as classes ATL **IPropertyPageImpl** (para implementar IPropertyPage) e **CDialogImpl**, que herda a classe ATL CDialogImpl (para gerenciar janelas e mensagens). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Provedor de serviços de exemplo**](sample-service-provider.md)
</dt> </dl>

 

 




