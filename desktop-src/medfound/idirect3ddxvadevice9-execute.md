---
description: Executa uma operação de decodificação de aceleração de vídeo DirectX (DXVA).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'Método IDirect3DDXVADevice9:: Execute (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772569"
---
# <a name="idirect3ddxvadevice9execute-method"></a>Método IDirect3DDXVADevice9:: execute

Executa uma operação de decodificação de aceleração de vídeo DirectX (DXVA).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FunctionNum* 
</dt> <dd>

Um **DWORD** que contém um ou mais números de função de DXVA. Para obter detalhes, consulte a [especificação DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pInputData* 
</dt> <dd>

Um ponteiro para um buffer que contém dados de entrada para a operação de decodificação. O significado desses dados depende do tipo de superfície e do número da função.

</dd> <dt>

*Incolocar* 
</dt> <dd>

O tamanho dos dados de entrada, em bytes.

</dd> <dt>

*OutputData* 
</dt> <dd>

Ponteiro para um buffer no qual o acelerador de vídeo grava dados de saída.

</dd> <dt>

*Sobrecolocações* 
</dt> <dd>

O tamanho do buffer *OutputData* , em bytes.

</dd> <dt>

*NumBuffers* 
</dt> <dd>

O número de elementos na matriz *pBufferInfo* .

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Um ponteiro para uma matriz de estruturas [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
