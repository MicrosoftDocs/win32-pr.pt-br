---
description: A interface IH323LineEx é implementada pelo H323 MSP e está disponível somente em objetos de endereço H. 323. Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interface IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754739"
---
# <a name="ih323lineex-interface"></a>Interface IH323LineEx

\[O **IH323LineEx** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **IH323LineEx** é implementada pelo [H323 MSP](h323-msp.md) e está disponível somente em objetos de endereço H. 323. Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP.

> [!Note]  
> Todos os métodos nesta interface devem ser chamados somente após o registro para chamadas de entrada nesse endereço.

 

## <a name="members"></a>Membros

A interface **IH323LineEx** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IH323LineEx** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IH323LineEx** tem esses métodos.



| Método                                                                                 | Descrição                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**Setalias**](ih323lineex-setalias.md)                                               | Configura um alias H. 323 padrão para o endereço.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configura o peso de preferência para os recursos padrão.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configura um endereço T. 120 externo para troca de dados.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

