---
description: Um URI que representa o identificador de serviço.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Elemento ServiceId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995103"
---
# <a name="serviceid-element"></a>Elemento ServiceId

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
| [**hospedeira**](host.md)<br/>     | Define os elementos **ServiceId** e [**Types**](types.md) para o host de serviço. Se não for fornecido explicitamente, o WSDAPI não fornecerá nenhum dado padrão em resposta a solicitações de metadados.<br/> <br/>                                                                                                                     |
| [**hospedado**](hosted.md)<br/> | Define os elementos **ServiceId** e [**Types**](types.md) para os serviços fornecidos por esse host de serviço. Cada serviço fornecido por esse host de serviço deve ter suas próprias informações de elemento [**hospedado**](hosted.md) para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




