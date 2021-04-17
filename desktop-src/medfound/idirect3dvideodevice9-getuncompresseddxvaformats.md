---
description: Obtém uma lista de formatos de pixel não compactados que podem ser processados usando um perfil de DXVA (DirectX Video Acceleration) especificado.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'Método IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296664"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>Método IDirect3DVideoDevice9:: GetUncompressedDXVAFormats

Obtém uma lista de formatos de pixel não compactados que podem ser processados usando um perfil de DXVA (DirectX Video Acceleration) especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Ponteiro para um GUID que especifica o perfil de DXVA. Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

Na entrada, especifica o número de elementos na matriz *pFormats* . Se *pFormats* for **NULL**, o valor de `*pNumFormats` deverá ser zero.

Na saída, se *pFormats* for **NULL**, *pNumFormats* receberá o número de formatos de pixel com suporte. Caso contrário, *pNumFormats* receberá o número real de formatos de pixel copiados para a matriz *pFormats* .

</dd> <dt>

*pFormats* 
</dt> <dd>

Endereço de uma matriz de valores **D3DFORMAT** ou **NULL**. Se o valor for não **nulo**, a matriz receberá uma lista de formatos de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Chame esse método duas vezes. Na primeira chamada, defina *pFormats* como **nulo**. O parâmetro *pNumFormats* recebe o número de formatos. Aloque uma matriz **D3DFORMAT** com o tamanho necessário e chame o método novamente. Desta vez, defina *pFormats* como o endereço da matriz. O método preenche a matriz com a lista de formatos de pixel.

O driver deve retornar os formatos em ordem decrescente de preferência, com o formato mais preferencial listado primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




