---
description: Um URI que representa o identificador de serviço.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc6ac1da57109f4f5671caf16a49b3a6174e7bfb63335d5ba15a548d7135990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756736"
---
# <a name="serviceid-element"></a>Elemento ServiceID

Um URI que representa o identificador de serviço.

## <a name="usage"></a>Uso

``` syntax
<ServiceID/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                             | Descrição                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Host**](host.md)<br/>     | Define os **elementos ServiceID** [**e Types**](types.md) para o host de serviço. Se não for fornecido explicitamente, o WSDAPI não fornecerá dados padrão em resposta a solicitações de metadados.<br/> <br/>                                                                                                                     |
| [**Hospedado**](hosted.md)<br/> | Define os **elementos ServiceID** e [**Types**](types.md) para os serviços fornecidos por esse host de serviço. Cada serviço fornecido por esse host [](hosted.md) de serviço deve ter suas próprias informações de elemento hospedado para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




