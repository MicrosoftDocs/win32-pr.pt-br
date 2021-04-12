---
description: Consulta o driver para obter a funcionalidade adicional Microsoft DirectDraw e Microsoft Direct3D que o driver suporta.
ms.assetid: 7169b672-5c61-4fca-860b-5ef426a7f925
title: Função NtGdiDdGetDriverInfo (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDriverInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2e9f78ed832015979c6768ec8f09e53ca8d2d4a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457010"
---
# <a name="ntgdiddgetdriverinfo-function"></a>Função NtGdiDdGetDriverInfo

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Consulta o driver para obter a funcionalidade adicional Microsoft DirectDraw e Microsoft Direct3D que o driver suporta.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdGetDriverInfo(
  _In_    HANDLE                hDirectDraw,
  _Inout_ PDD_GETDRIVERINFODATA puGetDriverInfoData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ no\]
</dt> <dd>

Identificador para objeto DirectDraw do modo de kernel criado anteriormente.

</dd> <dt>

*puGetDriverInfoData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [estrutura \_ GETDRIVERINFODATA do DD](https://msdn.microsoft.com/library/ms793868.aspx) que contém as informações necessárias para executar a consulta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdGetDriverInfo** retorna um dos seguintes códigos de retorno de chamada.



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

 

 




