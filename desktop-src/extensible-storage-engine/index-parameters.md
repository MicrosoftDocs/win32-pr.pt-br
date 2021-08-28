---
description: 'Saiba mais sobre: Parâmetros de índice'
title: Parâmetros de Índice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: f53430a6b624b6b65a5d02727dc16d7f1fba669d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470892"
---
# <a name="index-parameters"></a>Parâmetros de Índice


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="index-parameters"></a>Parâmetros de Índice

Este tópico contém parâmetros usados para o índice.

*JET_paramIndexTupleIncrement*  
132  

Esse parâmetro especifica o padrão para o incremento de deslocamento usado para passar pelo valor da coluna de origem ao gerar cada tupla. Para obter mais informações, consulte a [estrutura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dados.


| | | <p>Valor padrão:</p> | <p>1</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 - 32767</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e versões posteriores</p> | 



*JET_paramIndexTupleStart*  
133  

Esse parâmetro especifica o padrão para o deslocamento no valor da coluna de origem no qual a geração de tupla será iniciada. Para obter mais informações, consulte a [estrutura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dados.


| | | <p>Valor padrão:</p> | <p>0</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 - 32767</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e versões posteriores</p> | 



*JET_paramIndexTuplesLengthMax*  
111  

Esse parâmetro especifica o padrão para o comprimento máximo da tupla em um índice de tupla. Para obter mais informações, consulte a [estrutura JET_TUPLELIMITS](./jet-tuplelimits-structure.md) dados.

**Windows Vista:**  Antes de Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão. Por Windows Vista, não há mais suporte para isso.


| | | <p>Valor padrão:</p> | <p>10</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramIndexTuplesLengthMin*  
110  

Esse parâmetro especifica o padrão para o comprimento mínimo da tupla em um índice de tupla. Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obter mais informações.

**Windows Vista:**  Antes de Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão. Por Windows Vista, não há mais suporte para isso.


| | | <p>Valor padrão:</p> | <p>3</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0, 2-255</p><p><strong>Windows Vista:</strong> 2-255</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramIndexTuplesToIndexMax*  
112  

Esse parâmetro especifica o padrão para o comprimento máximo de uma cadeia de caracteres de origem para se quebrar em tuplas para um índice de tupla. Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obter mais informações.

**Windows Vista:**  Antes de Windows Vista, definir esse parâmetro como zero o definiria de volta para seu valor padrão. Por Windows Vista, não há mais suporte para isso.


| | | <p>Valor padrão:</p> | <p>32767</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 32767</p><p><strong>Windows Vista:</strong> 1 – 32767</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramUnicodeIndexDefault*  
72  

Esse parâmetro controla os parâmetros Unicode padrão usados por qualquer índice em uma coluna de chave Unicode. O tipo desse parâmetro é [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e é realmente passado usando um ponteiro de buffer armazenado no parâmetro integer [de JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md). O tamanho do buffer deve ser igual ao tamanho [de JET_UNICODEINDEX](./jet-unicodeindex-structure.md) e deve ser passado para [JetGetSystemParameter](./jetgetsystemparameter-function.md) usando o parâmetro de tamanho do buffer de cadeia de caracteres. Isso é claramente inconsistente, mas esse é o comportamento desse parâmetro.

O valor padrão desse parâmetro contém um LCID para a localidade em inglês dos EUA e os seguintes sinalizadores [LCMapStringW:](/windows/win32/api/winnls/nf-winnls-lcmapstringa)LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

**Windows 2000:**  A SORTID no LCID é ignorada. Um SORTID de SORT_DEFAULT sempre é usado.

**Windows 2000:**  Os [sinalizadores LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) devem conter os seguintes sinalizadores: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. Além disso, os [sinalizadores LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)podem conter os seguintes sinalizadores: NORM_IGNORENONSPACE.

**Observação**  Se o aplicativo quiser armazenar dados Unicode, é altamente recomendável que você não dependa dos parâmetros Unicode padrão para seus índices. O uso do inglês dos EUA é equivalente ao uso da localidade invariável e os sinalizadores [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)padrão são conhecidos por interferirem gravemente em alguns idiomas. Você sempre deve especificar suas próprias configurações para os parâmetros Unicode para JetCreateIndex2 usando [JET_INDEXCREATE](./jet-indexcreate-structure.md).


| | | <p>Valor padrão:</p> | <p>Especial</p> | | <p>Tipo:</p> | <p>JET_UNICODEINDEX* (JET_UNICODEINDEX)</p> | | <p>Intervalo válido:</p> | <p>Especial</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
