---
description: O método MergeEx do objeto de mesclagem é equivalente à função Merge, exceto pelo fato de que ele usa um argumento extra.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Método Merge. MergeEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757387"
---
# <a name="mergemergeex-method"></a>Método Merge. MergeEx

O método **MergeEx** do objeto de [**mesclagem**](merge-object.md) é equivalente à função [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , exceto pelo fato de que ele usa um argumento extra. O argumento *pConfiguration* é uma interface implementada pelo cliente. O argumento pode ser nulo. A presença desse argumento indica que o cliente é capaz de dar suporte à funcionalidade de configuração, mas não obriga o cliente a fornecer dados de configuração para qualquer item configurável específico.

O método [**Merge**](merge-merge.md) executa uma mesclagem do banco de dados atual e do módulo atual. A mesclagem anexa os componentes no módulo ao recurso identificado pelo *recurso*. A raiz da árvore de diretórios do módulo é redirecionada para o local fornecido pelo *RedirectDir*.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recurso* 
</dt> <dd>

O nome de um recurso no banco de dados.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

A chave de uma entrada na [tabela de diretório](directory-table.md) do banco de dados. Esse parâmetro pode ser nulo ou uma cadeia de caracteres vazia.

</dd> <dt>

*pConfiguration* 
</dt> <dd>

O argumento *pConfiguration* é uma interface implementada pelo cliente. O argumento pode ser nulo. A presença desse argumento indica que o cliente é capaz de dar suporte à funcionalidade de configuração, mas não obriga o cliente a fornecer dados de configuração para qualquer item configurável específico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando a mesclagem for concluída, os componentes no módulo serão anexados ao recurso identificado pelo *recurso*. Esse recurso não é criado e deve ser um recurso existente. O módulo pode ser anexado a recursos adicionais usando o método [**Connect**](merge-connect.md) .

As alterações feitas no banco de dados são salvas se e somente se o método [**CloseDatabase**](merge-closedatabase.md) for chamado com *BCommit* definido como **true**.

Se ocorrerem conflitos de mesclagem, incluindo exclusões, eles serão colocados no enumerador de erros para recuperação posterior, mas não causará falha na mesclagem. Os erros podem ser recuperados por meio da propriedade [**Errors**](merge-errors.md) . Erros e mensagens informativas são postados no arquivo de log atual.

Quando a mesclagem falha devido a uma configuração de módulo incorreta, a função [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) retorna E \_ falha. Isso inclui esses erros msmErrorType: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** e **msmErrorDataRequestFailed**. Esses erros fazem com que a mesclagem pare imediatamente quando o erro é encontrado. O objeto de erro ainda é adicionado ao enumerador quando **MergeEx** retorna E \_ falha. Para obter mais informações sobre erros de msmErrorType, consulte a [**\_ função obter tipo (objeto de erro)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Todos os outros erros fazem com que **MergeEx** retorne S \_ false e faça com que a mesclagem continue.

### <a name="c"></a>C++

Consulte a função [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
