---
description: Define o descritor de segurança associado ao compartilhamento DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Função NDdeSetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796402"
---
# <a name="nddesetsharesecurity-function"></a>Função NDdeSetShareSecurity

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Define o descritor de segurança associado ao compartilhamento DDE. Isso é feito normalmente após a edição da DACL atribuída ao compartilhamento DDE.

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*lpszShareName* \[ no\]
</dt> <dd>

O nome do compartilhamento cujo descritor de segurança deve ser modificado. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*si* \[ no\]
</dt> <dd>

Um valor de [**\_ informações de segurança**](/windows/desktop/SecAuthZ/security-information) que identifica as informações de segurança a serem recuperadas.

</dd> <dt>

*PSD* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contém informações de segurança. Este parâmetro não pode ser **nulo** e deve apontar para um descritor de segurança válido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

Para modificar o [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) associado a um compartilhamento DDE no DSDM, o usuário deve ter o privilégio apropriado; o criador de compartilhamento tem esse privilégio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) e **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**informações de segurança \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

