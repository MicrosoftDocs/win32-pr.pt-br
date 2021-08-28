---
description: 'Saiba mais sobre: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474122"
---
# <a name="jet_snp"></a>JET_SNP


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_snp"></a>JET_SNP

O **JET_SNP** de constantes descreve o tipo da operação para a qual as informações de progresso devem ser obtidas. Essas constantes são usadas como o *parâmetro snp* da [função JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) retorno de chamada.


| <p>Constante/valor</p> | <p>Descrição</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>O retorno de chamada é para uma operação de reparo.</p> | 
| <p>JET_snpCompact<br />4</p> | <p>O retorno de chamada é para desfragmentação de banco de dados.</p> | 
| <p>JET_snpRestore<br />8</p> | <p>O retorno de chamada é para uma operação de restauração.</p> | 
| <p>JET_snpBackup<br />9</p> | <p>O retorno de chamada é para uma operação de backup.</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>Não há suporte.</p><p><strong>Windows 2000:</strong>  O retorno de chamada é para a operação de atualização de formato de banco de dados.</p> | 
| <p>JET_snpScrub<br />11</p> | <p>O retorno de chamada é para uma operação de zero de banco de dados (ou seja, depuração).</p><p><strong>Windows Server 2003 e Windows 2000 Server:</strong>  Sem suporte.</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>O retorno de chamada é para o processo de atualização do formato de registro de todas as páginas de banco de dados.</p><p><strong>Windows Server 2003 e Windows 2000 Server:</strong>  Sem suporte.</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
