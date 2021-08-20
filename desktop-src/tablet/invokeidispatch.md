---
description: Invoca a funcionalidade auxiliar para a interface IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Função InvokeIDispatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 9708ebc5675d918c959be132d16037ac4e128650280b8243dcfe5c48834b602b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041866"
---
# <a name="invokeidispatch-function"></a>Função InvokeIDispatch

Invoca a funcionalidade auxiliar para a interface IDispatch.

Essa função não se destina a ser usada pelo código do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDispatch* 
</dt> <dd>

A instância da interface IDispatch.

</dd> <dt>

*Dispid* 
</dt> <dd>

O método, a propriedade ou o argumento a ser aprovado.

</dd> <dt>

*pDisp* 
</dt> <dd>

Os parâmetros a passar.

</dd> <dt>

*pVarResult* \[ out\]
</dt> <dd>

Uma estrutura que recebe os valores recuperados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, os possíveis códigos de retorno incluem, mas não estão limitados a, os valores mostrados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O valor de *pDispatch* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




