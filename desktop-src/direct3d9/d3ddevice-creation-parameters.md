---
description: Descreve os parâmetros de criação para um dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Estrutura de D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 64b3e13300d6c305d06b6b13db246134cb889cbfc407e4a99c6ae45adbf916e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805015"
---
# <a name="d3ddevice_creation_parameters-structure"></a>Estrutura de parâmetros de \_ criação de D3DDEVICE \_

Descreve os parâmetros de criação para um dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>Membros

<dl> <dt>

**AdapterOrdinal**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número ordinal que denota o adaptador de vídeo. \_O padrão D3DADAPTER é sempre o adaptador de vídeo primário. Use esse ordinal como o parâmetro do adaptador para qualquer um dos métodos [**IDirect3D9**](/windows/desktop/api) . Observe que diferentes instâncias de objetos do Direct3D 9,0 podem usar ordinais diferentes. Os adaptadores podem entrar ou sair de um sistema quando os usuários, por exemplo, adicionam ou removem monitores de um sistema de vários monitores ou quando alternam o hot-swap de um laptop. Consequentemente, use esse ordinal somente em uma instância do Direct3D 9,0 conhecida como válida, ou seja, o Direct3D 9,0 que criou essa interface [**IDirect3DDevice9**](/windows/desktop/api) ou o Direct3D 9,0 retornado de [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), conforme chamado por meio dessa interface **IDirect3DDevice9** .

</dd> <dt>

**DeviceType**
</dt> <dd>

Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) . Denota a quantidade de funcionalidade emulada para este dispositivo. O valor desse parâmetro espelha o valor passado para a chamada [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que criou este dispositivo.

</dd> <dt>

**hFocusWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de janela ao qual o foco pertence a este dispositivo Direct3D. O valor desse parâmetro espelha o valor passado para a chamada [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que criou este dispositivo.

</dd> <dt>

**BehaviorFlags**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Uma combinação de uma ou mais constantes [D3DCREATE](d3dcreate.md) que controlam o comportamento global do dispositivo. Essas constantes espelham as constantes passadas para [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) quando o dispositivo foi criado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
