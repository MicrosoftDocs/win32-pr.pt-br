---
description: A função PdhVbOpenQuery cria e inicializa uma estrutura de consulta exclusiva usada para gerenciar a coleção de dados de desempenho.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Função PdhVbOpenQuery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 70d207696f68b9ef86ba0bae1f596826bd6e400d05d011b330f67241e186f5eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962386"
---
# <a name="pdhvbopenquery-function"></a>Função PdhVbOpenQuery

A **função PdhVbOpenQuery** cria e inicializa uma estrutura de consulta exclusiva usada para gerenciar a coleção de dados de desempenho.

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [Funções de Contadores de Desempenho](performance-counters-functions.md).

Função PdhVbOpenQuery( \_ ByVal QueryHandle, desde \_ que )

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variável que é limpa (igual a 0) antes que a função seja chamada e, se a função for bem-sucedida, conterá a ID exclusiva da consulta que é criada e aberta. Esse identificador é usado nas chamadas subsequentes para outras funções PDH para identificar a consulta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará um **inteiro Longo** igual a ERROR SUCCESS e um novo handle na \_ *variável QueryHandle.*

Se a função falhar, o valor de retorno será um código [de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de erro [PDH](pdh-error-codes.md). A seguir estão os valores possíveis.



| Código de retorno                                                                                                     | Descrição                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**ARGUMENTO INVÁLIDO \_ PDH \_**</dt> </dl>           | O argumento é inválido ou incorreto.<br/>             |
| <dl> <dt>**FALHA NA \_ ALOCAÇÃO \_ DE MEMÓRIA PDH \_**</dt> </dl> | Não foi possível alocar um buffer de memória temporário.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

