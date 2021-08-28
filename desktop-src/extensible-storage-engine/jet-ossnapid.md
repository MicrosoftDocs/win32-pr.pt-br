---
description: 'Saiba mais sobre: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468363"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

O tipo de dados **JET_OSSNAPID** contém um identificador para um instantâneo do banco de dado.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Tipos de dados

JET_OSSNAPID

Um identificador para um instantâneo do banco de dados. Esse identificador é usado em elementos da API do JET que estão envolvidos no backup de instantâneo.

**NULL** pode ser usado para indicar um identificador inválido.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 


