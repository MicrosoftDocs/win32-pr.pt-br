---
description: Executa uma operação de decodificação de DXVA (Aceleração de Vídeo) do DirectX.
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: Método IDirect3DDXVADevice9::Execute (Dxva.h)
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
ms.openlocfilehash: ac00e5f78e4281523c006216f3173745ba26bc6429ddfdd9d74c9abbe616b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465956"
---
# <a name="idirect3ddxvadevice9execute-method"></a>Método IDirect3DDXVADevice9::Execute

Executa uma operação de decodificação de DXVA (Aceleração de Vídeo) do DirectX.

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

Uma **DWORD** que contém um ou mais números de função DXVA. Para obter detalhes, consulte a [especificação DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pInputData* 
</dt> <dd>

Um ponteiro para um buffer que contém dados de entrada para a operação de decodificação. O significado desses dados depende do tipo de superfície e do número da função.

</dd> <dt>

*InputSize* 
</dt> <dd>

O tamanho dos dados de entrada, em bytes.

</dd> <dt>

*OutputData* 
</dt> <dd>

Ponteiro para um buffer em que o acelerador de vídeo grava dados de saída.

</dd> <dt>

*OutputSize* 
</dt> <dd>

O tamanho do buffer *OutputData,* em bytes.

</dd> <dt>

*NumBuffers* 
</dt> <dd>

O número de elementos na matriz *pBufferInfo.*

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Um ponteiro para uma matriz de estruturas [**DXVABufferInfo.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
