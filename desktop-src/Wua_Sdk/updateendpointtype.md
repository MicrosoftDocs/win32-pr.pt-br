---
description: Define o tipo de pontos de extremidade que podem ser usados para se conectar a um serviço.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumeração UpdateEndpointType (UpdateEndpointAuth.h)
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
ms.openlocfilehash: 7fbfd67b3009fbe904284ea7a92cdea996d0a6e23a43a17639eb567d66536917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462906"
---
# <a name="updateendpointtype-enumeration"></a>Enumeração UpdateEndpointType

Define o tipo de pontos de extremidade que podem ser usados para se conectar a um serviço.

## <a name="syntax"></a>Sintaxe


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

Um ponto de extremidade cliente-servidor usado para se conectar ao serviço de atualização, como atualização do Windows, Microsoft Update e servidor WSUS em um ambiente corporativo, para encontrar informações sobre atualizações que podem ser aplicáveis ao computador.

O serviço de atualização retorna informações sobre atualizações que foram publicadas, revisadas ou retiradas desde a última vez que o cliente realizou uma sincronização com o servidor.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**
</dt> <dd>

Um ponto de extremidade de relatório que é usado quando o cliente relata os resultados de verificações, downloads e instala novamente no serviço de atualização.

No caso de serviços públicos (Windows Atualização e Microsoft Update), isso é feito para fins de monitoramento de qualidade.

No caso de serviços privados, como um servidor WSUS corporativo, esse tipo de ponto de extremidade também permite que o servidor colete inventário e outras informações sobre os computadores cliente sob gerenciamento.

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**
</dt> <dd>

Um ponto de extremidade de atualização automática que é usado quando o computador cliente contata um serviço de atualização para ver se há uma nova versão do software cliente Windows Update Agent.

O ponto de extremidade de auto-atualização usa um protocolo diferente do ponto de extremidade do Client-Server para que as auto-atualizações possam ser distribuídas mesmo se houver uma condição de erro que possa estar impedindo que a sincronização normal de cliente-servidor funciona em um computador cliente específico.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**
</dt> <dd>

Um ponto de extremidade de regulamento que é usado quando o computador cliente contata o serviço de regulamento para agir em uma atualização específica aplicável ao computador de destino.

O serviço de regulamentação pode indicar se a atualização é "regulamentada" (também conhecida como "acelerada") – em outras palavras, o serviço de regulamentação pode dizer ao computador cliente que ela não deve agir em uma atualização específica, embora essa atualização pareça ser aplicável.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**
</dt> <dd>

Um ponto de extremidade de direcionamento simples que é usado somente com serviços privados (servidores WSUS em ambientes corporativos). Em um ambiente corporativo, os computadores cliente podem ser atribuídos a grupos de destino específicos e as atualizações podem ser aprovadas para instalação em computadores em alguns grupos, mas não em outros.

Por exemplo, o administrador do WSUS pode criar um grupo de "Teste" para computadores que são usados para testar novas atualizações, e o administrador pode aprovar atualizações recém-lançadas para instalação em computadores no grupo Teste sem aplá-las para instalação em outros computadores na organização. A troca de direcionamento simples é usada para permitir que um computador cliente se registre no servidor do WSUS e permitir que o servidor diga ao computador cliente em qual grupo ele está.

</dd> <dt>

<span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**
</dt> <dd>

Um ponto de extremidade de cliente-cliente seguro que permite que um cliente obtenha informações sobre aplicativos que precisam de licenciamento para que possam ser usados em um computador cliente. Atualmente, essa estrutura de licenciamento é usada apenas pelo Windows 8 para implantar aplicativos e atualizações obtidos por meio da Windows Store. No momento, o ponto de extremidade do servidor-cliente seguro não é usado pelo Windows Update, Microsoft Update ou WSUS.

</dd> <dt>

<span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**
</dt> <dd>

O ponto de extremidade de autenticação de serviço secundário é usado por um cliente para fornecer autenticação antes de obter informações sobre aplicativos que precisam de licenciamento para que possam ser usados em um computador cliente. Atualmente, essa estrutura de licenciamento só é utilizada pelo Windows 8 para implantar aplicativos e atualizações obtidos por meio da Windows Store. No momento, o ponto de extremidade de autenticação de serviço secundário não é usado pelo Windows Update, Microsoft Update ou WSUS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                              |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



 

 




