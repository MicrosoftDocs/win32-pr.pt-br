---
description: Registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Função ShellDDEInit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968123"
---
# <a name="shellddeinit-function"></a>Função ShellDDEInit

Registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.

## <a name="syntax"></a>Sintaxe


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*init* \[ no\]
</dt> <dd>

Tipo: **bool**

**True** para registrar o processo atual como host DDE; **False** para cancelar o registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O processo que chama essa função atua como o Shell e é usado para exibir o conteúdo das pastas abertas com o verbo ' Open ' de [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

Essa função não tem um cabeçalho ou arquivo de biblioteca associado, portanto, ele deve ser chamado pelo valor ordinal. Chame [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da DLL (Shdocvw.dll) para obter um identificador de módulo. Em seguida, chame o [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e a função número ordinal 118 para obter o endereço da função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de desktop do Windows XP, Windows 2000 Professional \[\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (versão 6,0 ou posterior)</dt> </dl> |



 

 
