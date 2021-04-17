---
description: Passa um valor de chave com todos os dados associados exigidos pelo módulo de descriptografia de conteúdo para o sistema de chaves fornecido.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'Método IMFMediaKeySession:: Update'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105787556"
---
# <a name="imfmediakeysessionupdate-method"></a>Método IMFMediaKeySession:: Update

Passa um valor de chave com todos os dados associados exigidos pelo módulo de descriptografia de conteúdo para o sistema de chaves fornecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* 
</dt> <dd></dd> <dt>

*CB* 
</dt> <dd>

A contagem em bytes de *chave*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




