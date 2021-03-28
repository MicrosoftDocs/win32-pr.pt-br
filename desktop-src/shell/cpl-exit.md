---
description: Enviado uma vez para a função CPlApplet de um aplicativo do painel de controle antes que a DLL que contém o aplicativo do painel de controle seja liberada.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Mensagem de CPL_EXIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164312"
---
# <a name="cpl_exit-message"></a>Mensagem de saída de CPL \_

Enviado uma vez para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle antes que a DLL que contém o aplicativo do painel de controle seja liberada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.

## <a name="remarks"></a>Comentários

Essa mensagem é enviada depois que a última mensagem de [**\_ parada de CPL**](cpl-stop.md) é enviada.

Em resposta a essa mensagem, um aplicativo do painel de controle deve liberar qualquer memória alocada e executar a limpeza em nível global.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
