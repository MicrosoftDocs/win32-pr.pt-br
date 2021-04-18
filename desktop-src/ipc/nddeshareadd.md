---
description: Cria e adiciona um novo compartilhamento DDE ao Gerenciador de banco de dados de compartilhamento DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Função NDdeShareAdd (Nddeapi. h)
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
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789524"
---
# <a name="nddeshareadd-function"></a>Função NDdeShareAdd

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Cria e adiciona um novo compartilhamento DDE ao Gerenciador de banco de dados de compartilhamento DDE (DSDM).

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

*lpszServer* \[ no\]
</dt> <dd>

O nome do servidor cujo DSDM deve ser modificado.

</dd> <dt>

*nLevel* \[ no\]
</dt> <dd>

O nível de informações. Esse parâmetro deve ser 2.

</dd> <dt>

*PSD* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) a ser associado a esse compartilhamento e no qual as verificações de acesso serão executadas em logons subsequentes para esse compartilhamento. Esse parâmetro pode ser **nulo** e, nesse caso, o DSDM cria um descritor de segurança padrão que concede "controle total" ao proprietário e "ler e vincular" a todos.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Um ponteiro para a estrutura [**NDDESHAREINFO**](nddeshareinfo-str.md) que define a lista ApplicationTopic associada ao compartilhamento DDE que está sendo criado, bem como outros parâmetros. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*cBufSize* \[ no\]
</dt> <dd>

O tamanho da estrutura *lpBuffer* , em bytes. Este parâmetro não pode ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.

Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Comentários

Antes que um cliente possa se conectar ao compartilhamento de DDE, ele deve ser confiável com [**NDdeSetTrustedShare**](nddesettrustedshare.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **NDdeShareAddW** (Unicode) e **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

