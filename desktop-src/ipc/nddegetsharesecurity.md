---
description: Recupera o descritor de segurança associado ao compartilhamento DDE. Isso é feito normalmente para edição.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Função NDdeGetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837056"
---
# <a name="nddegetsharesecurity-function"></a>Função NDdeGetShareSecurity

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Recupera o descritor de segurança associado ao compartilhamento DDE. Isso é feito normalmente para edição.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor no qual o DSDM reside.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento cujo descritor de segurança deve ser recuperado do DSDM. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*si* \[ no\]
</dt> <dd>

Um valor de [**\_ informações de segurança**](/windows/desktop/SecAuthZ/security-information) que especifica as informações de segurança a serem recuperadas do descritor de segurança associado ao compartilhamento.

</dd> <dt>

*PSD* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que recebe o descritor de segurança auto-relativo. Este parâmetro pode ser **NULL**. Se esse parâmetro for **NULL**, o DSDM determinará o tamanho das informações de segurança solicitadas e retornará o número de bytes necessários no parâmetro *lpcbsdRequired* juntamente com o \_ código de erro NDDE buf \_ muito \_ pequeno.

</dd> <dt>

*cbSD* \[ no\]
</dt> <dd>

O tamanho do buffer *PSD* . Esse parâmetro deverá ser zero se o *PSD* for **nulo**.

</dd> <dt>

*lpcbsdRequired* \[ fora\]
</dt> <dd>

Um ponteiro para a variável que recebe o tamanho real do descritor de segurança recuperado. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se o parâmetro *PSD* era **nulo**, ele retornará NDDE \_ buf \_ muito \_ pequeno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeGetShareSecurityW** (Unicode) e **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**informações de segurança \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

