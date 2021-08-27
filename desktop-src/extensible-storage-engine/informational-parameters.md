---
description: 'Saiba mais sobre: parâmetros informativos'
title: Parâmetros informativos
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: cd932f64956e1a00aae5925b97dbf6c35ecc2661
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987599"
---
# <a name="informational-parameters"></a>Parâmetros informativos


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="informational-parameters"></a>Parâmetros informativos

Este tópico contém parâmetros que são usados para expor informações sobre o mecanismo de banco de dados.

*JET_paramKeyMost*  
134  

Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitido que pode ser selecionado para o tamanho da página do banco de dados atual (conforme configurado por JET_paramDatabasePageSize).


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>JET_cbKeyMost4KBytePage</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>255 – 65535</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>N/D</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>N/D</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>a partir do Windows Server 2008 e Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Esse parâmetro somente leitura retorna o [JET_COLTYP](./jet-coltyp.md) máximo (JET_coltypMax) para essa versão do mecanismo de banco de dados. Esse valor pode ser usado para testar o suporte de um [JET_COLTYP](./jet-coltyp.md)específico. Se um determinado [JET_COLTYP](./jet-coltyp.md) for menor que o valor desse parâmetro, ele será suportado pelo mecanismo de banco de dados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>JET_coltypUnsignedShort + 1</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0 a 255</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>N/D</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>N/D</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>a partir do Windows Server 2008 e Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Parâmetro somente leitura que retorna o tamanho da parte de valor longo com base no tamanho da página configurada. Se um valor longo for para ser lido ou gravado com várias chamadas de coluna Jet {Set, Retrieve}, o uso de um buffer cujo tamanho é um múltiplo do tamanho da parte é mais eficiente.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>2 KB página = 1966 bytes<br />página de 4 KB = 4014 bytes<br />8 KB página = 8110 bytes<br />16 KB página = 4050 bytes<br />32 KB página = 8150 bytes</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0-10000</p> | 
| <p>Escopo:</p> | <p></p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p></p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p></p> | 
| <p>Afeta o layout físico:</p> | <p></p> | 
| <p>Afeta a confiabilidade:</p> | <p></p> | 
| <p>Afeta o desempenho:</p> | <p></p> | 
| <p>Afeta os recursos:</p> | <p></p> | 
| <p>Disponibilidade:</p> | <p></p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
