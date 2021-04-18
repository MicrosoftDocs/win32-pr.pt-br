---
description: Inicia o processamento para criar uma imagem decodificada.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'Método IDirect3DDXVADevice9:: BeginFrame (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793610"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>Método IDirect3DDXVADevice9:: BeginFrame

Inicia o processamento para criar uma imagem decodificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDstSurface* 
</dt> <dd>

Um ponteiro para a interface **IDirect3DSurface9** da superfície de destino descompactada.

</dd> <dt>

*SizeInputData* 
</dt> <dd>

O tamanho do buffer especificado por *pInputData*, em bytes. O valor deve ser 2.

</dd> <dt>

*pInputData* 
</dt> <dd>

Ponteiro para um buffer que contém dados para o acelerador de vídeo. Esse buffer deve conter o índice de quadro baseado em zero, especificado como um valor de **palavra** .

</dd> <dt>

*pSizeOutputData* 
</dt> <dd>

O tamanho do buffer especificado por *pOutputData*, em bytes. O valor deve ser zero.

</dd> <dt>

*pOutputData* 
</dt> <dd>

Ponteiro para um buffer no qual o acelerador de vídeo pode gravar. Defina esse parâmetro como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Para cada chamada para **BeginFrame**, o decodificador deve fazer uma chamada correspondente para [**IDirect3DDXVADevice9:: endframe**](idirect3ddxvadevice9-endframe.md).

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

 

 




