---
description: A função IsWindowRedirectedForPrint determina se a janela especificada é redirecionada no momento para impressão.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Função IsWindowRedirectedForPrint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764309"
---
# <a name="iswindowredirectedforprint-function"></a>Função IsWindowRedirectedForPrint

A função **IsWindowRedirectedForPrint** determina se a janela especificada é redirecionada no momento para impressão.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

O identificador de janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a janela for redirecionada no momento para impressão, a função retornará um valor diferente de zero; caso contrário, retornará zero.

## <a name="remarks"></a>Comentários

Uma janela é redirecionada para impressão quando processa uma chamada para a [**janela**](/windows/desktop/api/Winuser/nf-winuser-printwindow)do. Em uma chamada para o **diwindow**, uma janela renderiza seu conteúdo para um contexto de dispositivo fora da tela.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Janela**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**impressão do WM \_**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**WM \_ FILEclient**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

