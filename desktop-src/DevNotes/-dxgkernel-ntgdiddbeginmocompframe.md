---
description: Inicia a decodificação de um novo quadro.
ms.assetid: da2c231d-89a9-4fd9-99b5-f7c1309c26e0
title: Função NtGdiDdBeginMoCompFrame (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBeginMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45c359092d1a161aae7671c437fdb9683a2a8eb9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500834"
---
# <a name="ntgdiddbeginmocompframe-function"></a>Função NtGdiDdBeginMoCompFrame

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Inicia a decodificação de um novo quadro.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdBeginMoCompFrame(
  _In_    HANDLE                   hMoComp,
  _Inout_ PDD_BEGINMOCOMPFRAMEDATA puBeginFrameData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMoComp* \[ no\]
</dt> <dd>

Identificador para uma [**estrutura \_ \_ local MOTIONCOMP DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contém uma descrição da compensação de movimento que está sendo solicitada.

</dd> <dt>

*puBeginFrameData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ BEGINMOCOMPFRAMEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) que contém as informações necessárias para iniciar a decodificação de um novo quadro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdBeginMoCompFrame** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

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

 

 
