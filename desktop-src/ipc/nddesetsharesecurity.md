---
description: Define o descritor de segurança associado ao compartilhamento DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Função NDdeSetShareSecurity (Nddeapi.h)
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
ms.openlocfilehash: 00e6d8c4b235e8f7d02ba22e737fc4de9bf4a739864afb1464e6f84c620faa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481820"
---
# <a name="nddesetsharesecurity-function"></a>Função NDdeSetShareSecurity

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

Define o descritor de segurança associado ao compartilhamento DDE. Isso geralmente é feito depois de editar a DACL atribuída ao compartilhamento DDE.

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

*lpszServer* \[ Em\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*lpszShareName* \[ Em\]
</dt> <dd>

O nome do compartilhamento cujo descritor de segurança deve ser modificado. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*si* \[ Em\]
</dt> <dd>

Um [**valor \_ DE INFORMAÇÕES**](/windows/desktop/SecAuthZ/security-information) DE SEGURANÇA que identifica as informações de segurança a recuperar.

</dd> <dt>

*pSD* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**\_ SECURITY DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contém informações de segurança. Esse parâmetro não pode ser **NULL** e deve apontar para um descritor de segurança válido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NDDE \_ NO \_ ERROR.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

Para modificar [**o \_ DESCRITOR DE SEGURANÇA associado**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) a um compartilhamento DDE no DSDM, o usuário deve ter o privilégio apropriado; o criador do compartilhamento tem esse privilégio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) e **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**INFORMAÇÕES DE \_ SEGURANÇA**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

