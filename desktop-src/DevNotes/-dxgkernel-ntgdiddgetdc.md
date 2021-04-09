---
description: Cria um DC (contexto de dispositivo) para a superfície especificada.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Função NtGdiDdGetDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089189"
---
# <a name="ntgdiddgetdc-function"></a>Função NtGdiDdGetDC

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Cria um DC (contexto de dispositivo) para a superfície especificada.

## <a name="syntax"></a>Sintaxe


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador para uma superfície DirectDraw do modo kernel retornada anteriormente por [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) ou [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).

</dd> <dt>

*puColorTable* \[ no\]
</dt> <dd>

Ponteiro para uma tabela de cores de substituição para o DC retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedida, essa função retornará um **HDC** válido; caso contrário, ele retornará **NULL**.

## <a name="remarks"></a>Comentários

Somente um DC é permitido por superfície em um determinado momento. As chamadas subsequentes para **NtGdiDdGetDC** falharão até que o controlador de domínio anterior seja liberado.

Os aplicativos são aconselhados a chamar [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) em vez disso, que fornece a mesma funcionalidade de uma maneira independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
