---
description: Renderiza primitivos e retorna o estado de renderização atualizado.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Função NtGdiD3DDrawPrimitives2 (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010131"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>Função NtGdiD3DDrawPrimitives2

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Renderiza primitivos e retorna o estado de renderização atualizado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCmdBuf* \[ no\]
</dt> <dd>

Manipule a estrutura [**\_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica a superfície do DirectDraw que contém os dados do comando.

</dd> <dt>

*hVBuf* \[ no\]
</dt> <dd>

Manipule a estrutura [**\_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica a superfície do DirectDraw que contém os dados do vértice.

</dd> <dt>

*pded* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma estrutura [**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) que contém as informações necessárias para o driver processar um ou mais primitivos.

</dd> <dt>

*pfpVidMemCmd* \[ entrada, saída\]
</dt> <dd>

Novo ponteiro para memória de vídeo se o driver permutau o buffer de comando.

</dd> <dt>

*pdwSizeCmd* \[ entrada, saída\]
</dt> <dd>

Especifica o número mínimo de bytes para os quais o driver deve aumentar o buffer do comando de permuta.

</dd> <dt>

*pfpVidMemVtx* \[ entrada, saída\]
</dt> <dd>

Novo ponteiro para memória de vídeo se o driver permutau o buffer de vértice.

</dd> <dt>

*pdwSizeVtx* \[ entrada, saída\]
</dt> <dd>

Especifica o número mínimo de bytes que o driver deve alocar para o buffer de vértice de permuta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiD3DDrawPrimitives2** retorna um dos seguintes códigos de retorno de chamada.



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

 

 
