---
description: Encerra o processamento para criar uma imagem decodificada.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'Método IDirect3DDXVADevice9:: endframe (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090968"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>Método IDirect3DDXVADevice9:: endframe

Encerra o processamento para criar uma imagem decodificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SizeMiscData* 
</dt> <dd>

O tamanho do buffer especificado por *pMiscData*, em bytes. O valor deve ser 2.

</dd> <dt>

*pMiscData* 
</dt> <dd>

Ponteiro para um buffer que contém dados para o acelerador de vídeo. Esse buffer deve conter o mesmo índice de quadro que foi passado para o método [**IDirect3DDXVADevice9:: BeginFrame**](idirect3ddxvadevice9-beginframe.md) no parâmetro *pInputData* .

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

 

 




