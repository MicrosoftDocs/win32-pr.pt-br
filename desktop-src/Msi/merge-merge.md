---
description: O método Merge do objeto Merge executa uma mesclagem do banco de dados atual e do módulo atual.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Método Merge. Merge (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751436"
---
# <a name="mergemerge-method"></a>Método Merge. Merge

O método **Merge** do objeto [**Merge**](merge-object.md) executa uma mesclagem do banco de dados atual e do módulo atual. A mesclagem anexa os componentes no módulo ao recurso identificado pelo *recurso*. A raiz da árvore de diretórios do módulo é redirecionada para o local fornecido pelo *RedirectDir*.

O método **Merge** só pode ser chamado uma vez para mesclar uma combinação específica de arquivos. msi e. msm.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.Merge(
  Feature,
  RedirectDir
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

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando a mesclagem for concluída, os componentes no módulo serão anexados ao recurso identificado pelo *recurso*. Esse recurso não é criado e deve ser um recurso existente. Observe que o método **Merge** obtém todas as referências de recurso no módulo e substitui a referência de recurso para todas as ocorrências do GUID NULL no banco de dados do módulo. Para obter mais informações, consulte [fazendo referência a recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).

O módulo pode ser anexado a recursos adicionais usando o método [**Connect**](merge-connect.md) . Observe que chamar o método **Connect** somente cria associações de componente de recurso. Ele não modifica as linhas que já foram mescladas no banco de dados.

As alterações feitas no banco de dados são salvas se e somente se o método [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) for chamado com *BCommit* definido como **true**.

Se ocorrerem conflitos de mesclagem, incluindo exclusões, eles serão colocados no enumerador de erros para recuperação posterior, mas não causará falha na mesclagem. Os erros podem ser recuperados por meio da propriedade [**Errors**](error-object.md) . Erros e mensagens informativas são postados no arquivo de log atual.

### <a name="c"></a>C++

Consulte [**mesclar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
