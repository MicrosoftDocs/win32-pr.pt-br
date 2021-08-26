---
description: A classe FOURCCMap fornece conversão entre subtipos de mídia GUID e marcas de mídia de 32 bits FOURCC de estilo antigo.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Classe FOURCCMap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: a0ba22ce288535a8d940a5f70275f0152ffa559090d820b77df06ed3d1a9178d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043257"
---
# <a name="fourccmap-class"></a>Classe FOURCCMap

![hierarquia de classe FOURCCMap](images/fourcc01.png)

A classe **FOURCCMap** fornece conversão entre subtipos de mídia **GUID** e marcas de mídia de 32 bits **FOURCC** de estilo antigo. nas APIs de multimídia originais do Windows, os tipos de mídia foram marcados com valores de 32 bits criados a partir de caracteres de 4 8 bits e eram conhecidos como s **FOURCC**. DirectShow tipos de mídia têm **GUID** s para o subtipo, parcialmente porque são mais simples de criar (a criação de um novo **FOURCC** requer seu registro com a Microsoft). Como os s **FOURCC** são exclusivos, um mapeamento um-para-um tornou-se possível alocando um intervalo de 4.000.000.000 **GUID** s representando os s **FOURCC**. Esse intervalo é todos os **GUIDs** do formulário:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Essa classe simplifica a conversão entre o **GUID** s e os s **FOURCC**. Isso é apenas para fins de compatibilidade. É recomendável que todos os novos subtipos de mídia sejam representados por **GUID** s criados por Guidgen.exe ou por uma ferramenta semelhante, e não pelo mapeamento de s **FOURCC**.

O objeto é derivado de um **GUID**, sem membros de dados adicionais e pode ser convertido em um **GUID**. O objeto pode ser passado como um **FOURCC** no momento da construção. O construtor padrão inicializará o **FOURCC** como zero.

Os métodos [**GetFOURCC**](fourccmap-getfourcc.md) e [**SetFOURCC**](fourccmap-setfourcc.md) não verificam se as partes fixas do **GUID** correspondem ao intervalo **FOURCC** . Portanto, se você converter um ponteiro para um **GUID** em um ponteiro para um **FOURCC** e, em seguida, definir ou obter o campo **FOURCC** , também precisará verificar separadamente se o **GUID** está dentro do intervalo **FOURCC** .

## <a name="member-functions"></a>Funções de membro



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Método de construtor.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Recupera o **FOURCC** de um objeto **FOURCCMap** .    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Define a parte **FOURCC** do objeto **FOURCCMap** . |



 

 

 



