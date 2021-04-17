---
description: A interface IProvidePropertyBuilder, quando implementada, permite que os objetos especifiquem objetos do construtor de propriedades para propriedades.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interface IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752768"
---
# <a name="iprovidepropertybuilder-interface"></a>Interface IProvidePropertyBuilder

A interface **IProvidePropertyBuilder** , quando implementada, permite que os objetos especifiquem objetos do construtor de propriedades para propriedades. Os construtores são invocados por um botão de reticências ( \[ ... \] ) no navegador de propriedades Microsoft Visual Studio e é invocado por meio de [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quando o botão é pressionado. Para fornecer um construtor para uma determinada propriedade, retorne um GUID para o construtor de propriedades que deve ser invocado para a propriedade atual de [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md). Os construtores geralmente são implementados por meio de caixas de diálogo modais.

A versão desta interface é 1,0. As chamadas de método são recebidas em um ponto de extremidade atribuído dinamicamente (conforme descrito na documentação binária do MSMQ no mapeamento de ponto de extremidade) e usam o UUID (identificador universal exclusivo) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".

## <a name="members"></a>Membros

A interface **IProvidePropertyBuilder: IUnknown** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IProvidePropertyBuilder** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IProvidePropertyBuilder: IUnknown** tem esses métodos.



| Método                                                                       | Descrição                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md)             | Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.<br/> |
| [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md) | Verifica se um construtor deve ser associado a uma determinada propriedade.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



 

 
