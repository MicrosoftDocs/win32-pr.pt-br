---
description: registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.
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
ms.openlocfilehash: 27d2e304cf3a67f522bbeec4835f5faa98b24d1509363873bb51387391f94b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676708"
---
# <a name="shellddeinit-function"></a>Função ShellDDEInit

registra os serviços de troca dinâmica de dados de Shell (DDE) no processo atual, notificando o sistema de que o processo atual deseja hospedar objetos DDE.

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
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional \[ aplicativos de área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shdocvw.dll (versão 6,0 ou posterior)</dt> </dl> |



 

 
