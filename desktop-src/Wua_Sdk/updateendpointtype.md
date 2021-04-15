---
description: Define o tipo de pontos de extremidade que podem ser usados para se conectar a um serviço.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumeração UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501329"
---
# <a name="updateendpointtype-enumeration"></a>Enumeração UpdateEndpointType

Define o tipo de pontos de extremidade que podem ser usados para se conectar a um serviço.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**
</dt> <dd>

Um ponto de extremidade cliente-servidor usado para se conectar ao serviço de atualização, como Windows Update, Microsoft Update e servidor WSUS em um ambiente corporativo, para encontrar informações sobre atualizações que podem ser aplicáveis ao computador.

O serviço de atualização retorna informações sobre atualizações que foram publicadas, revisadas ou retiradas desde a última vez que o cliente realizou uma sincronização com o servidor.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

Um ponto de extremidade de relatório que é usado quando o cliente relata os resultados de verificações, downloads e instalações de volta para o serviço de atualização.

No caso de serviços públicos (Windows Update e Microsoft Update), isso é feito para fins de monitoramento de qualidade.

No caso de serviços privados, como um servidor WSUS corporativo, o thhis tipo de ponto de extremidade também permite que o servidor colete inventário e outras informações sobre os computadores cliente sob gerenciamento.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

Um ponto de extremidade de autoatualização que é usado quando o computador cliente entra em contato com um serviço de atualização para ver se há uma nova versão do software cliente do agente de Windows Update.

O ponto de extremidade de autoatualização usa um protocolo diferente do ponto de extremidade Client-Server para que as autoatualizações possam ser distribuídas mesmo se houver uma condição de erro que possa estar impedindo que a sincronização normal do cliente-servidor funcione em um computador cliente específico.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Um ponto de extremidade de regulamentação que é usado quando o computador cliente entra em contato com o serviço regulamento para agir em uma atualização específica aplicável ao computador de destino.

O serviço regulamento pode indicar se a atualização é "regulamentada" (também conhecida como "limitada") – em outras palavras, o serviço de regulamentação pode informar ao computador cliente que ele não deve atuar em uma atualização específica, embora essa atualização pareça ser aplicável.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

Um ponto de extremidade de direcionamento simples que é usado somente com serviços privados (servidores WSUS em ambientes corporativos). Em um ambiente corporativo, os computadores cliente podem ser atribuídos a grupos de destino específicos e as atualizações podem ser aprovadas para instalação em computadores em alguns grupos, mas não em outros.

Por exemplo, o administrador do WSUS pode criar um grupo de "teste" para computadores que são usados para testar novas atualizações, e o administrador pode aprovar atualizações lançadas recentemente para instalação em computadores no grupo de teste sem aprová-los para instalação em outros computadores da organização. A troca de direcionamento simples é usada para permitir que um computador cliente se registre no servidor do WSUS e para permitir que o servidor informe ao computador cliente em qual grupo ele está.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Um ponto de extremidade de cliente/servidor protegido que permite que um cliente obtenha informações sobre aplicativos que precisam de licenciamento para que eles possam ser usados em um computador cliente. Atualmente, essa estrutura de licenciamento é usada apenas pelo Windows 8 para implantar aplicativos e atualizações que são obtidas por meio da Windows Store. O ponto de extremidade do servidor de cliente protegido não é usado atualmente por Windows Update, Microsoft Update ou WSUS.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

O ponto de extremidade de autenticação de serviço secundário é usado por um cliente para fornecer autenticação antes de obter informações sobre aplicativos que precisam de licenciamento para que eles possam ser usados em um computador cliente. Atualmente, essa estrutura de licenciamento é utilizada apenas pelo Windows 8 para implantar aplicativos e atualizações que são obtidas por meio da Windows Store. O ponto de extremidade de autenticação de serviço secundário não é usado atualmente por Windows Update, Microsoft Update ou WSUS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                              |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




