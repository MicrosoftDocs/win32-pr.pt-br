---
description: Determina o local de um recurso com o tipo e o nome especificados no módulo especificado.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: Função FindResourceWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169446"
---
# <a name="findresourcewrapw-function"></a>Função FindResourceWrapW

\[O **FindResourceWrapW** está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Em vez disso, você deve usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]

Determina o local de um recurso com o tipo e o nome especificados no módulo especificado.

> [!Note]  
> **FindResourceWrapW** é um wrapper para a função **FindResourceW** . Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HMODULE* \[ no\]
</dt> <dd>

Tipo: **HMODULE**

Um identificador para o módulo cujo arquivo executável contém o recurso. Um valor **NULL** especifica o identificador de módulo associado ao arquivo de imagem que o sistema operacional usou para criar o processo atual.

</dd> <dt>

*lpName* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

O nome do recurso. Para obter mais informações, consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lpType* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para uma cadeia de caracteres que especifica o tipo de recurso. Para obter mais informações, consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRSRC**

Se a função for realizada com sucesso, o valor de retorno será um identificador para o bloco de informações do recurso especificado. Para obter um identificador para o recurso, passe esse identificador para a função [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

Se a função falhar, o valor de retorno será **nulo**. Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Comentários

Se você precisar especificar uma localização específica, use a função [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) em vez de **FindResourceWrapW**.

O **FindResourceWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais mais antigos. O método preferencial é usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) em conjunto com a camada Microsoft para Unicode (MSLU).

**FindResourceWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 66.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Nenhum</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
