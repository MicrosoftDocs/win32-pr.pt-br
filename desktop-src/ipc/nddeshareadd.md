---
description: Cria e adiciona um novo compartilhamento DDE ao DSDM (gerenciador de banco de dados de compartilhamento DDE).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Função NDdeShareAdd (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 0a02381fad8412c7ada0c337c21e633ffa6793887a720ec504f1dfa3d78d9ede
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602136"
---
# <a name="nddeshareadd-function"></a>Função NDdeShareAdd

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

Cria e adiciona um novo compartilhamento DDE ao DSDM (gerenciador de banco de dados de compartilhamento DDE).

## <a name="syntax"></a>Sintaxe


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszServer* \[ Em\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*nLevel* \[ Em\]
</dt> <dd>

O nível de informações. Esse parâmetro deve ser 2.

</dd> <dt>

*pSD* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**\_ SECURITY DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) a ser associada a esse compartilhamento e no qual as verificações de acesso serão executadas nos inícios subsequentes desse compartilhamento. Esse parâmetro pode ser **NULL,** caso em que o DSDM cria um descritor de segurança padrão que concede "Controle Total" ao proprietário e "Ler e Vincular" a todos.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Um ponteiro para a estrutura [**NDINFO que**](nddeshareinfo-str.md) define a lista ApplicationTopic associada ao compartilhamento DDE que está sendo criado, bem como outros parâmetros. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*cBufSize* \[ Em\]
</dt> <dd>

O tamanho da estrutura *lpBuffer,* em bytes. Esse parâmetro não pode ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NDDE \_ NO \_ ERROR.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

Antes que um cliente possa se conectar ao compartilhamento DDE, ele deve ser confiável com [**NDdeSetTrustedShare.**](nddesettrustedshare.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeShareAddW** (Unicode) e **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDINFOAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

