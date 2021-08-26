---
description: Usado pelo serviço de notificação de eventos do sistema do Microsoft Internet Explorer (SENS) para acessar o armazenamento de dados de eventos. Essa interface estende a interface IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interface IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6ecee3137750da9f86b61696799a3a7c6e7177beb2b92fb386712a6c90f69d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070596"
---
# <a name="ieventsystem2-interface"></a>Interface IEventSystem2

Usado pelo serviço de notificação de eventos do sistema do Microsoft Internet Explorer (SENS) para acessar o armazenamento de dados de eventos. Essa interface estende a interface [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .

## <a name="when-to-implement"></a>Quando implementar

Você não precisa implementar a interface **IEventSystem2** . Um objeto de sistema de eventos fornecido pelo sistema (CLSID \_ CEventSystem) implementa **IEventSystem2**.

## <a name="when-to-use"></a>Quando usar

Se você usar o SENS, poderá chamar os métodos de **IEventSystem2** para adicionar e remover objetos de e para o repositório de eventos e para obter objetos do repositório de eventos.

Como [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) e o objeto Publicador não têm mais suporte, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) não é chamado no método [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .

## <a name="members"></a>Membros

A interface **IEventSystem2** herda de **IEventSystem**. **IEventSystem2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEventSystem2** tem esses métodos.



| Método                                                                         | Descrição                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**Obter versão**](ieventsystem2-getversion.md)                                 | Recupera o número de versão do sistema de eventos.<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | Verifica a existência de todos os assinantes transitórios no repositório de dados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

