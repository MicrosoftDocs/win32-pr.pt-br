---
description: Uma solicitação para atualizar o estado inicial de um objeto; por exemplo, uma textura ou sombreador.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IUpdateObject::UpdateObject
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b48e206d09c784ac2f2df31eeab0d65cac04f740a66874fe9e436f96b8349143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282266"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>Método IUpdateObject::UpdateObject

Uma solicitação para atualizar o estado inicial de um objeto; por exemplo, uma textura ou sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a>Parâmetros

*objectAddress*   
A ID do objeto a ser atualizado.

*Tamanho*   
O tamanho da carga de atualização em bytes.

*buffer \_ count1*   
O payload de atualização.

*Pcallback*   
O endereço de uma função usada para notificar o host de que o objeto foi atualizado.

## <a name="return-value"></a>Retornar valor

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IUpdateObject**](/windows/desktop/direct3dtools/iupdateobject)

 

 
