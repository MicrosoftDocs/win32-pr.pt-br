---
description: A interface IH323LineEx é implementada pelo H323 MSP e está disponível somente em objetos de endereço H.323. Essa interface expõe métodos que permitem a criação e a manipulação de terminais que podem se comunicar entre clientes H323 e SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interface IH323LineEx (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 856deae92568acd2eb9f9394e949dc2d5ea6a4bbde9c2c28f0b998c99098eef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013106"
---
# <a name="ih323lineex-interface"></a>Interface IH323LineEx

\[**IH323LineEx** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A interface **IH323LineEx** é implementada pelo [H323 MSP](h323-msp.md) e está disponível somente em objetos de endereço H.323. Essa interface expõe métodos que permitem a criação e a manipulação de terminais que podem se comunicar entre clientes H323 e SDP.

> [!Note]  
> Todos os métodos nessa interface devem ser chamados somente após o registro para chamadas de entrada nesse endereço.

 

## <a name="members"></a>Membros

A interface **IH323LineEx** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IH323LineEx** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IH323LineEx** tem esses métodos.



| Método                                                                                 | Descrição                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | Configura um alias H.323 padrão para o endereço.<br/>             |
| [**SetDefaultCapabilityPrefault**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configura a ponderação de preferência para recursos padrão.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configura um endereço T.120 externo para troca de dados.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

