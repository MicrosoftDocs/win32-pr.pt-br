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
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296732"
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

*fRestoreCache* \[ no\]
</dt> <dd>

Tipo: **bool**

**True** para restaurar o cache de imagem do sistema do disco; Caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

**True** se o cache tiver sido atualizado com êxito, **false** se a inicialização falhou.

## <a name="remarks"></a>Comentários

Se você estiver usando listas de imagens do sistema em seu próprio processo, deverá chamar **FileIconInit** nos seguintes horários:

-   Na inicialização.
-   Em resposta a uma mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) quando o sinalizador [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) é definido.

**FileIconInit** não está incluído em um arquivo de cabeçalho. Você deve chamá-lo diretamente do Shell32.dll, usando o ordinal 660.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
