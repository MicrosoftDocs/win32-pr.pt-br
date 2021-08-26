---
title: Função RasAdminGetErrorString (Rassapi. h)
description: A função RasAdminGetErrorString recupera uma cadeia de caracteres de mensagem que corresponde a um código de erro RAS retornado por uma das funções de administração do servidor RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- Função RasAdminGetErrorString RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45c768daef7c889351744c5e046c83f4de7e220f59752c1db271067efb68366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028597"
---
# <a name="rasadmingeterrorstring-function"></a>Função RasAdminGetErrorString

\[essa função é fornecida somente para compatibilidade com versões anteriores com o Windows NT Server 4,0. ele retorna uma \_ chamada \_ de erro não \_ implementada no Windows Server 2003. Os aplicativos devem usar a função [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]

A função **RasAdminGetErrorString** recupera uma cadeia de caracteres de mensagem que corresponde a um código de erro RAS retornado por uma das funções de administração do servidor RAS (RasAdmin). Essas cadeias de caracteres de mensagem são recuperadas do Rasmsg.dll que é instalado como parte do RAS.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceId* \[ no\]
</dt> <dd>

Especifica um código de erro retornado por uma das funções RasAdmin. Esse valor deve estar no intervalo de códigos de erro de RASBASE para RASBASEEND. Eles são definidos em Raserror. h.

</dd> <dt>

*lpszString* \[ fora\]
</dt> <dd>

Ponteiro para um buffer que recebe a mensagem de erro que corresponde ao código de erro especificado.

</dd> <dt>

*InBufSize* \[ no\]
</dt> <dd>

Especifica o tamanho, em caracteres, do buffer *lpszString* . Normalmente, as mensagens de erro são de 80 caracteres ou menos; um tamanho de buffer de 512 caracteres é sempre adequado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro. Esse valor pode ser um último valor de erro definido pelas funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)ou [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) ; ou pode ser um dos seguintes códigos de erro.



| Valor                                                                                                      | Significado                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>   | Os parâmetros *ResourceId* ou *lpszString* são inválidos.<br/>      |
| <dl> <dt>**ERRO \_ de \_ buffer insuficiente**</dt> </dl> | O tamanho especificado pelo parâmetro *InBufSize* é muito pequeno.<br/> |



 

Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

As funções RasAdmin podem retornar códigos de erro que não estão no intervalo com suporte da função **RasAdminGetErrorString** . Por exemplo, as funções RasAdmin podem retornar códigos de erro que são definidos em Lmerr. h e Winerror. h. Antes de chamar **RasAdminGetErrorString**, verifique se o código de erro está no intervalo RASBASE para RASBASEEND, conforme definido em Raserror. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/> | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Biblioteca<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Funções de administração do servidor RAS](ras-server-administration-functions.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**Cadeia de caracteres LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

