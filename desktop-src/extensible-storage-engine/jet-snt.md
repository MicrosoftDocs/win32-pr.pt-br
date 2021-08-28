---
description: 'Saiba mais sobre: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 250ad992ec26b218bab21691f26c0938b6be6921
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481382"
---
# <a name="jet_snt"></a>JET_SNT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_snt"></a>JET_SNT

O [JET_SNT]() de constantes descreve os pontos do progresso de uma operação sobre quais informações são solicitadas em uma chamada para a [função JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) retorno de chamada.


| <p>Constante/valor</p> | <p>Descrição</p> | 
|-----------------------|--------------------|
| <p>JET_sntBegin<br />5</p> | <p>O início de uma operação</p> | 
| <p>JET_sntRequirements<br />7</p> | <p>Sem suporte.</p><p><strong>Windows 2000 Server:</strong>  A operação é iniciada. Nesse caso, o último parâmetro da função de retorno de chamada deve ser um ponteiro válido para uma estrutura <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> que indica o número total de unidades a serem executadas.</p> | 
| <p>JET_sntProgress<br />0</p> | <p>O número de unidades concluídas e o número de unidades ainda a serem feitas. Essas informações são retornadas nos membros de uma <a href="gg269328(v=exchg.10).md">estrutura JET_SNPROG</a> dados.</p> | 
| <p>JET_sntComplete<br />6</p> | <p>A conclusão de uma operação.</p> | 
| <p>JET_sntFail<br />3</p> | <p>A falha de uma operação.</p> | 
| <p>JET_sntRecoveryStep<br />8</p> | <p>O controle de recuperação de uma operação.</p><div class="alert">&gt; [!NOTE]&gt; <P>Esse valor não é aplicável a versões do sistema operacional Windows a partir do Windows 8.</P></div> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
