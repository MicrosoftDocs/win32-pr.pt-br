---
title: Interfaces para provedores de conteúdo seguro
description: Interfaces para provedores de conteúdo seguro
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- referência de programação, conteúdo protegido por DRM
- referência para Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Conteúdo protegido por DRM
- Windows Media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- referência de programação, provedor de conteúdo seguro (SCP)
- referência para Windows Media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- provedor de conteúdo seguro (SCP)
- SCP (provedor de conteúdo seguro)
- Windows Media Gerenciador de Dispositivos, interfaces SCP
- Gerenciador de Dispositivos, interfaces SCP
- referência de programação, interfaces SCP
- referência para Windows Media Gerenciador de Dispositivos, interfaces SCP
- Interfaces SCP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788810"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfaces para provedores de conteúdo seguro

Um SCP (provedor de conteúdo seguro) é um componente de plug-in que permite que o Windows Media Gerenciador de Dispositivos transfira e solicite informações de direitos do conteúdo protegido por DRM. A Microsoft fornece um componente SCP que pode manipular arquivos WMA e WMV protegidos por DRM. Se seu dispositivo ou aplicativo usar o conteúdo protegido por DRM de outros formatos, ele deverá criar um componente SCP implementando todas essas interfaces. Caso contrário, não será necessário usar essas interfaces.



| Interface                                                  | Descrição                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | A principal interface do provedor de conteúdo seguro.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Estende o **ISCPSecureAuthenticate** fornecendo uma maneira de obter um objeto de sessão.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Usado para trocar conteúdo protegido e direitos associados ao conteúdo.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Estende o **ISCPSecureExchange** fornecendo uma nova versão do método **TransferContainerData** .                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Estende o **ISCPSecureExchange2** fornecendo um desempenho de troca de dados aprimorado e um método de retorno de chamada de transferência completa.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Consultado pelo Windows Media Gerenciador de Dispositivos para determinar a propriedade do conteúdo protegido.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Estende o **ISCPSecureQuery** por meio de funcionalidade que determina se o provedor de conteúdo seguro é responsável pelo conteúdo e, nesse caso, fornece uma URL para atualizar os componentes revogados e determinar quais componentes foram revogados. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Estende o **ISCPSecureQuery2** fornecendo um conjunto de novos métodos para recuperar os direitos e tomar decisão em um canal claro.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Fornece gerenciamento de Estado comum eficiente para várias operações.                                                                                                                                                                                  |



 

 

 




