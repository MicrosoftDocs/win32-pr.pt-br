---
description: Inicializa ou reinicializa a lista de imagens do sistema.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: Função FileIconInit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 1771e1f0bde83f0fc7d070787b7a19f87007e26bd1ad42dcaa88e230e61a60af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111806"
---
# <a name="fileiconinit-function"></a>Função FileIconInit

Inicializa ou reinicializa a lista de imagens do sistema.

## <a name="syntax"></a>Sintaxe


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fRestoreCache* \[ Em\]
</dt> <dd>

Tipo: **BOOL**

**TRUE** para restaurar o cache de imagem do sistema do disco; **FALSE caso** contrário, .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **BOOL**

**TRUE** se o cache foi atualizado com êxito, **FALSE** se a inicialização falhou.

## <a name="remarks"></a>Comentários

Se você estiver usando listas de imagens do sistema em seu próprio processo, deverá chamar **FileIconInit** nos seguintes momentos:

-   Na iniciação.
-   Em resposta a uma [**mensagem WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) quando o [**sinalizador SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) é definido.

**FileIconInit** não está incluído em um arquivo de título. Você deve chamá-lo diretamente do Shell32.dll, usando o ordinal 660.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
