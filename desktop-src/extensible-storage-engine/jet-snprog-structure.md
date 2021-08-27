---
description: 'Saiba mais sobre: estrutura de JET_SNPROG'
title: Estrutura de JET_SNPROG
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
ms.openlocfilehash: 7e5590bb5be133c380e30168cca8d1d693fb6fea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466763"
---
# <a name="jet_snprog-structure"></a>Estrutura de JET_SNPROG


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_snprog-structure"></a>Estrutura de JET_SNPROG

A estrutura de **JET_SNPROG** contém informações sobre o progresso de uma operação de execução longa. Quando a função de retorno de chamada é chamada para notificar o status da operação e a operação ainda está em andamento, o último parâmetro da função de retorno de chamada é um ponteiro para uma estrutura de **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura de **JET_SNPROG** , em bytes. Esse valor confirma a presença dos campos a seguir.

**cunitDone**

O número de unidades de trabalho que já foram concluídas durante a função de execução longa.

**cunitTotal**

O número de unidades de trabalho que precisam ser concluídas. Esse valor deve ser sempre maior ou igual a **cunitDone**.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 


