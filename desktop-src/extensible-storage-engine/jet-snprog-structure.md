---
description: 'Saiba mais sobre: estrutura JET_SNPROG dados'
title: estrutura JET_SNPROG de JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987729"
---
# <a name="jet_snprog-structure"></a>estrutura JET_SNPROG de JET_SNPROG


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_snprog-structure"></a>estrutura JET_SNPROG de JET_SNPROG

A **JET_SNPROG** contém informações sobre o progresso de uma operação de execução longa. Quando a função de retorno de chamada é chamada para notificar o status da operação e a operação ainda está em andamento, o último parâmetro da função de retorno de chamada é um ponteiro para uma estrutura **JET_SNPROG.**

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membros

**Cbstruct**

O tamanho da estrutura **JET_SNPROG,** em bytes. Esse valor confirma a presença dos campos a seguir.

**cunitDone**

O número de unidades de trabalho que já foram concluídas durante a função de execução longa.

**cunitTotal**

O número de unidades de trabalho que precisam ser concluídas. Esse valor sempre deve ser maior ou igual a **cunitDone**.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 


