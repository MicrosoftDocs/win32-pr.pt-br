---
description: Enviado para a função CPlApplet de um Painel de Controle para solicitar que ele execute a inicialização global, especialmente a alocação de memória.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: CPL_INIT mensagem (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be6acdf58822e6f10f35880a97a7b5bbb9ce0b7bbbf7556b4c18c3f7ad96f72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456366"
---
# <a name="cpl_init-message"></a>Mensagem \_ CPL INIT

Enviado para a [**função CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo Painel de Controle para solicitar que ele execute a inicialização global, especialmente a alocação de memória.


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a inicialização for bem-sucedida, [**a função CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deverá retornar diferentes de zero. Caso contrário, ele deverá retornar zero.

Se [**CPlApplet retornar**](/windows/win32/api/cpl/nc-cpl-applet_proc) zero, o aplicativo de controle terminará a comunicação e liberará a DLL que contém o Painel de Controle aplicativo.

## <a name="remarks"></a>Comentários

Como essa é a única maneira Painel de Controle aplicativo pode sinalizar uma condição de erro, o aplicativo deve alocar memória em resposta a essa mensagem.

Essa mensagem é enviada imediatamente após a DLL que contém o aplicativo ser carregada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Freelibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
