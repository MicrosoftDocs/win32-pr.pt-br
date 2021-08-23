---
title: Interfaces para provedores de conteúdo seguros
description: Interfaces para provedores de conteúdo seguros
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Mídia Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- referência de programação, conteúdo protegido por DRM
- referência para Windows mídia Gerenciador de Dispositivos, conteúdo protegido por DRM
- Conteúdo protegido por DRM
- Windows SCP (provedor de conteúdo seguro) Gerenciador de Dispositivos mídia
- Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- referência de programação, provedor de conteúdo seguro (SCP)
- referência para Windows media Gerenciador de Dispositivos, provedor de conteúdo seguro (SCP)
- provedor de conteúdo seguro (SCP)
- SCP (provedor de conteúdo seguro)
- Windows Interfaces Gerenciador de Dispositivos mídia, interfaces SCP
- Gerenciador de Dispositivos, interfaces SCP
- referência de programação, interfaces SCP
- referência para Windows mídia Gerenciador de Dispositivos, interfaces SCP
- Interfaces SCP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80b74cfc50fb6dcf328379c5c46696dc2ee097e2ed5c2507a2a4f14676efd85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119247336"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfaces para provedores de conteúdo seguros

Um SCP (provedor de conteúdo seguro) é um componente de plug-in que permite que o Windows Media Gerenciador de Dispositivos transfira e solicite informações de direitos do conteúdo protegido por DRM. A Microsoft fornece um componente SCP que pode lidar com arquivos WMA e WMV protegidos por DRM. Se seu dispositivo ou aplicativo usar conteúdo protegido por DRM de outros formatos, ele deverá criar um componente SCP implementando todas essas interfaces. Caso contrário, você não precisará usar essas interfaces.



| Interface                                                  | Descrição                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | A interface primária do provedor de conteúdo seguro.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Estende **ISCPSecureAuthenticate** fornecendo uma maneira de obter um objeto de sessão.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Usado para trocar conteúdo protegido e direitos associados ao conteúdo.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Estende **ISCPSecureExchange** fornecendo uma nova versão do **método TransferContainerData.**                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Estende **ISCPSecureExchange2** fornecendo melhor desempenho de troca de dados e um método de retorno de chamada completo de transferência.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Consultado por Windows mídia Gerenciador de Dispositivos para determinar a propriedade do conteúdo protegido.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Estende **ISCPSecureQuery** por meio da funcionalidade que determina se o provedor de conteúdo seguro é responsável pelo conteúdo e, nesse caso, fornece uma URL para atualizar componentes revogados e determinar quais componentes foram revogados. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Estende **ISCPSecureQuery2** fornecendo um conjunto de novos métodos para recuperar os direitos e tomar decisões em um canal claro.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Fornece gerenciamento de estado comum eficiente para várias operações.                                                                                                                                                                                  |



 

 

 




