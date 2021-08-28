---
description: 'Saiba mais sobre: Constantes de alça inválidas'
title: Constantes de alça inválidas
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: 28a52b2fc7a51572cc7bb78ad7631df41438310a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473272"
---
# <a name="invalid-handle-constants"></a>Constantes de alça inválidas


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="invalid-handle-constants"></a>Constantes de alça inválidas

As constantes a seguir indicam alças inválidas para diferentes aspectos do ESE.


| <p>Constante/valor</p> | <p>Descrição</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br />(~(JET_INSTANCE)0)</p> | <p>Um alça inválido para uma instância de banco de dados.<br /><strong>Windows XP:</strong> Introduzido no Windows XP.</p> | 
| <p>JET_sesidNil<br />(~(JET_SESID)0)</p> | <p>Um alça inválido para uma ID de sessão.</p> | 
| <p>JET_tableidNil<br />(~(JET_TABLEID)0)</p> | <p>Um alça inválido para uma ID de tabela.</p> | 
| <p>JET_bitNil<br />((JET_GRBIT)0)</p> | <p>Um alça inválido para um grupo de bits.</p> | 
| <p>JET_LSNil<br />(~(JET_LS)0)</p> | <p>Um alça inválido para o local Armazenamento.</p> | 
| <p>JET_dbidNil<br />((JET_DBID) 0xFFFFFFFF)</p> | <p>Um alça inválido para a ID do banco de dados.</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 


