---
description: Obtém uma lista de formatos de pixel descompactados que podem ser renderizados usando um perfil DXVA (Aceleração de Vídeo DirectX) especificado.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: Método IDirect3DVideoDevice9::GetUncompressedDXVAFormats (Dxva.h)
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
ms.openlocfilehash: 3d7f27060d0c9e43f1852c86697826986c0c095c14a19fbfafa53978e96cbe79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878793"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>Método IDirect3DVideoDevice9::GetUncompressedDXVAFormats

Obtém uma lista de formatos de pixel descompactados que podem ser renderizados usando um perfil DXVA (Aceleração de Vídeo DirectX) especificado.

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

*Pguid* 
</dt> <dd>

Ponteiro para um GUID que especifica o perfil DXVA. Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

Na entrada, especifica o número de elementos na matriz *pFormats.* Se *pFormats* for **NULL,** o valor de `*pNumFormats` deverá ser zero.

Na saída, se *pFormats* for **NULL,** *pNumFormats* receberá o número de formatos de pixel com suporte. Caso contrário, *pNumFormats* receberá o número real de formatos de pixel copiados para a *matriz pFormats.*

</dd> <dt>

*pFormats* 
</dt> <dd>

Endereço de uma matriz de **valores D3DFORMAT** ou **NULL.** Se o valor for não **NULL,** a matriz receberá uma lista de formatos de pixel.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Chame esse método duas vezes. Na primeira chamada, de definir *pFormats* como **NULL.** O *parâmetro pNumFormats* recebe o número de formatos. Aloce **uma matriz D3DFORMAT** com o tamanho necessário e chame o método novamente. Desta vez, de definir *pFormats* como o endereço da matriz. O método preenche a matriz com a lista de formatos de pixel.

O driver deve retornar os formatos em ordem decrescente de preferência, com o formato mais preferencial listado primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




