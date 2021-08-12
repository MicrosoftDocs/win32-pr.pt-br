---
description: Define a rampa de gama para o dispositivo.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Função NtGdiDdSetGammaRamp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 78e68a76fed6db78a2f3d247c5bec1b73f3df3b6fe204e0d09b1bc5f14a014b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668805"
---
# <a name="ntgdiddsetgammaramp-function"></a>Função NtGdiDdSetGammaRamp

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Define a rampa de gama para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ no\]
</dt> <dd>

Identificador para o objeto de driver de modo kernel para o qual a rampa deve ser definida.

</dd> <dt>

*HDC* \[ no\]
</dt> <dd>

Reservado.

</dd> <dt>

*lpGammaRamp* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de estruturas **DDGAMMARAMP** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno será **true** se a função for bem-sucedida. Caso contrário, será **nulo**.

## <a name="remarks"></a>Comentários

Recomenda-se que os aplicativos usem os métodos **IDirectDrawGammaControl:: SetGammaRamp** ou [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , pois esses métodos oferecem a mesma funcionalidade independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
