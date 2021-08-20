---
description: O método Merge do objeto Merge executa uma mesclagem do banco de dados atual e do módulo atual.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Método Merge.Merge (Mergemod.h)
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
ms.openlocfilehash: 43644f8ef19b81331f9f2d88d4dac03d654379d51174a50e994d3642cb86eabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804726"
---
# <a name="mergemerge-method"></a>Método Merge.Merge

O **método Merge** do objeto [**Merge**](merge-object.md) executa uma mesclagem do banco de dados atual e do módulo atual. A mesclagem anexa os componentes no módulo ao recurso identificado pelo *Recurso*. A raiz da árvore de diretório do módulo é redirecionada para o local determinado por *RedirectDir*.

O **método Merge** só pode ser chamado uma vez para mesclar uma combinação específica de arquivos .msi e .msm.

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

A chave de uma entrada na tabela [Diretório do](directory-table.md) banco de dados. Esse parâmetro pode ser nulo ou uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Depois que a mesclagem for concluída, os componentes do módulo serão anexados ao recurso identificado pelo *Recurso*. Esse recurso não é criado e deve ser um recurso existente. Observe que o **método Merge** obtém todas as referências de recurso no módulo e substitui a referência de recurso para todas as ocorrências do GUID nulo no banco de dados do módulo. Para obter mais informações, consulte [Referenciando recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).

O módulo pode ser anexado a recursos adicionais usando o [**Conexão**](merge-connect.md) método . Observe que chamar o **método Conexão** cria apenas associações de componente de recurso. Ele não modifica as linhas que já foram mescladas no banco de dados.

As alterações feitas no banco de dados serão salvas se e somente se o [**método CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) for chamado com *bCommit* definido como **TRUE.**

Se ocorrerem conflitos de mesclagem, incluindo exclusões, eles serão colocados no enumerador de erro para recuperação posterior, mas não causará falha na mesclagem. Os erros podem ser recuperados por meio [**da propriedade**](error-object.md) Erros. Erros e mensagens informativas são postados no arquivo de log atual.

### <a name="c"></a>C++

Consulte [**Função Merge.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
