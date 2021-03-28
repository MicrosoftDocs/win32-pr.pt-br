---
description: Enviado para a função CPlApplet de um aplicativo de painel de controle para solicitar que ele execute a inicialização global, especialmente a alocação de memória.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Mensagem de CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967351"
---
# <a name="cpl_init-message"></a>CPL \_ mensagem de inicialização

Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo de painel de controle para solicitar que ele execute a inicialização global, especialmente a alocação de memória.


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

## <a name="return-value"></a>Retornar valor

Se a inicialização for realizada com sucesso, a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deverá retornar diferente de zero. Caso contrário, ele deve retornar zero.

Se [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retornar zero, o aplicativo de controle terminará a comunicação e liberará a DLL que contém o aplicativo do painel de controle.

## <a name="remarks"></a>Comentários

Como essa é a única maneira como um aplicativo do painel de controle pode sinalizar uma condição de erro, o aplicativo deve alocar memória em resposta a essa mensagem.

Essa mensagem é enviada imediatamente depois que a DLL que contém o aplicativo é carregada.

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

 

 
