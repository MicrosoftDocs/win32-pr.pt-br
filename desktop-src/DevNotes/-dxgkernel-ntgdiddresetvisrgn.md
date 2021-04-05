---
description: Usado para habilitar o modo de usuário para obter uma compreensão válida da região de recorte para Windows na área de trabalho. Esse recorte pode ser alterado de forma assíncrona do ponto de vista de threads do modo de usuário.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Função NtGdiDdResetVisrgn (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826136"
---
# <a name="ntgdiddresetvisrgn-function"></a>Função NtGdiDdResetVisrgn

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Usado para habilitar o modo de usuário para obter uma compreensão válida da região de recorte para Windows na área de trabalho. Esse recorte pode ser alterado de forma assíncrona do ponto de vista de threads do modo de usuário.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ no\]
</dt> <dd>

Ponteiro para o objeto de modo de usuário de qualquer superfície que pertence ao dispositivo do DirectDraw para o qual o recorte deve ser redefinido. Para obter detalhes, consulte a documentação do DDK.

</dd> <dt>

*HWND* \[ no\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

O recorte pode ser alterado de forma assíncrona do ponto de vista de threads do modo de usuário. As partes do modo kernel do DirectDraw e do Windows Graphics Device Interface (GDI) mantêm um contador que é incrementado sempre que a lista de recorte de toda a área de trabalho é alterada. Uma chamada para essa função registra esse contador com cada superfície primária do DirectDraw existente no sistema.

Posteriormente, quando uma dessas superfícies primárias for modificada por uma operação [IDirectDrawSurface7:: Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) ou [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) (consulte a documentação do DDK), o contador registrado com a superfície será comparado com o contador global. Se esses valores forem diferentes, um código de erro DDERR \_ VISRGNCHANGED será retornado para o código do modo de usuário. O código de modo de usuário então consultará novamente o recorte atual para a área de trabalho, chamará **NtGdiDdResetVisrgn** e tentará novamente o IDirectDrawSurface7:: Blt aplicado à superfície primária, respeitando o novo recorte. Eventualmente, o recorte que foi amostrado pelo código do modo de usuário será o mesmo que o recorte atual de Propriedade do modo kernel, e o IDirectDrawSurface7:: Blt terá permissão para continuar.

Os aplicativos são aconselhados a usar a interface [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) ou o método [IDirect3DDevice8::P reenviado](/previous-versions/ms889707(v=msdn.10)) para lidar com alterações de recorte assíncrono. Essas construções implementam recorte assíncrono em uma maneira automatizada e independente do sistema operacional.

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

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
