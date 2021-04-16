---
description: Usado para bloquear uma área especificada de memória de buffer e fornecer um ponteiro válido para um bloco de memória associado ao buffer.
ms.assetid: 6f2ecefa-376c-4f6c-a031-666dd992f96a
title: Função NtGdiDdLockD3D (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c049d37e3507f5bf4429b6ffd5d8ec03327640e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750291"
---
# <a name="ntgdiddlockd3d-function"></a>Função NtGdiDdLockD3D

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Usado para bloquear uma área especificada de memória de buffer e fornecer um ponteiro válido para um bloco de memória associado ao buffer.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdLockD3D(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ no\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície associada à região da memória a ser bloqueada.

</dd> <dt>

*puLockData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ LOCKDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) que contém as informações necessárias para executar o bloqueio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdLockD3D** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

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

 

 
