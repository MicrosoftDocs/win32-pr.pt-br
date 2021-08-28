---
description: 'Saiba mais sobre: Parâmetros informacionais'
title: Parâmetros informacionais
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
ms.openlocfilehash: 62adda8c818124b905cf81a2114cddd6556c3d13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469523"
---
# <a name="informational-parameters"></a>Parâmetros informacionais


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="informational-parameters"></a>Parâmetros informacionais

Este tópico contém parâmetros usados para expor informações sobre o mecanismo de banco de dados.

*JET_paramKeyMost*  
134  

Esse parâmetro somente leitura indica o comprimento máximo de chave de índice permitida que pode ser selecionado para o tamanho atual da página do banco de dados (conforme configurado por JET_paramDatabasePageSize).


| | | <p>Valor padrão:</p> | <p>JET_cbKeyMost4KBytePage</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>255 – 65535</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>N/D</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>N/D</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>A partir do Windows Server 2008 e Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Esse parâmetro somente leitura retorna o [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) máximo para essa versão do mecanismo de banco de dados. Esse valor pode ser usado para testar o suporte de [um](./jet-coltyp.md)JET_COLTYP . Se um determinado [JET_COLTYP](./jet-coltyp.md) for menor que o valor desse parâmetro, ele será suportado pelo mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>JET_coltypUnsignedShort + 1</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 – 255</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>N/D</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>N/D</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>A partir do Windows Server 2008 e Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Parâmetro somente leitura que retorna o tamanho da parte de valor longo com base no tamanho da página configurado. Se um valor longo deve ser lido ou gravado com várias chamadas Jet{Set,Retrieve}Column, usar um buffer cujo tamanho é um múltiplo do tamanho da parte é mais eficiente.


| | | <p>Valor padrão:</p> | <p>Página de 2kb = 1966 bytes<br />Página de 4kb = 4014 bytes<br />Página de 8kb = 8110 bytes<br />Página de 16kb = 4050 bytes<br />Página 32kb = 8150 bytes</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-10000</p> | | <p>Escopo:</p> | <p></p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p></p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p></p> | | <p>Afeta o layout físico:</p> | <p></p> | | <p>Afeta a confiabilidade:</p> | <p></p> | | <p>Afeta o desempenho:</p> | <p></p> | | <p>Afeta recursos:</p> | <p></p> | | <p>Disponibilidade:</p> | <p></p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
