---
title: Estrutura FONTDIRENTRY
description: Contém informações sobre uma fonte individual em um grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menus de estrutura FONTDIRENTRY e outros recursos
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e236104730dbbfe79ec0ed3d18cbb465402ed8827c6037a2457bec18faf63024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886736"
---
# <a name="fontdirentry-structure"></a>Estrutura FONTDIRENTRY

Contém informações sobre uma fonte individual em um grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**dfVersion**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Um número de versão definido pelo usuário para os dados de recurso que as ferramentas podem usar para ler e gravar arquivos de recursos.

</dd> <dt>

**dfSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho do arquivo, em bytes.

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Tipo: **Char**

</dd> <dd>

As informações de direitos autorais do fornecedor de fontes.

</dd> <dt>

**dfType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tipo de arquivo de fonte.

</dd> <dt>

**dfPoints**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tamanho do ponto em que esse conjunto de caracteres tem a melhor aparência.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A resolução vertical, em pontos por polegada, na qual esse conjunto de caracteres foi digitalizado.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A resolução horizontal, em pontos por polegada, na qual esse conjunto de caracteres foi digitalizado.

</dd> <dt>

**dfAscent**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A distância da parte superior de uma célula de definição de caractere para a linha de base da fonte tipográfica.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A quantidade de entrelinha dentro dos limites definidos pelo membro **dfPixHeight** . As marcas de acentuação e outros caracteres diacríticos podem ocorrer nessa área.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A quantidade de entrelinha extra que o aplicativo adiciona entre linhas.

</dd> <dt>

**dfItalic**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Uma fonte em itálico se não for igual a zero.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Uma fonte sublinhada se não for igual a zero.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Uma fonte riscada se não for igual a zero.

</dd> <dt>

**dfWeight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O peso da fonte no intervalo de 0 a 1000. Por exemplo, 400 é romano e 700 é negrito. Se esse valor for zero, será usado um peso padrão. Para obter valores adicionais definidos, consulte a descrição da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfCharSet**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O conjunto de caracteres da fonte. Para valores predefinidos, consulte a descrição da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A largura da grade na qual uma fonte de vetor foi digitalizada. Para fontes de varredura, se o membro não for igual a zero, ele representará a largura de todos os caracteres no bitmap. Se o membro for igual a zero, a fonte terá caracteres de largura variável.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A altura do bitmap de caractere para fontes de rasterização ou a altura da grade na qual uma fonte de vetor foi digitalizada.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

A inclinação e a família da fonte. Para obter informações adicionais, consulte a descrição da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A largura média de caracteres na fonte (geralmente definida como a largura da letra x). Esse valor não inclui a folga necessária para caracteres em negrito ou itálico.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

A largura do caractere mais largo na fonte.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O primeiro código de caractere definido na fonte.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O último código de caractere definido na fonte.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O caractere para substituir os caracteres que não estão na fonte.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O caractere que será usado para definir quebras de palavras para justificação de texto.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O número de bytes em cada linha do bitmap. Esse valor é sempre mesmo para que as linhas iniciem em limites de palavras. Para fontes de vetor, esse membro não tem significado.

</dd> <dt>

**dfDevice**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O deslocamento no arquivo para uma cadeia de caracteres terminada em nulo que especifica um nome de dispositivo. Para uma fonte genérica, esse valor é zero.

</dd> <dt>

**dfFace**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O deslocamento no arquivo para uma cadeia de caracteres terminada em nulo que nomeia a face de tipo.

</dd> <dt>

**dfReserved**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Esse membro é reservado.

</dd> <dt>

**Szdevicename**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

O nome do dispositivo se esse arquivo de fonte for designado para um dispositivo específico.

</dd> <dt>

**szFaceName**
</dt> <dd>

Tipo: **CHAR**

</dd> <dd>

O nome da face de tipo da fonte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Há uma estrutura **FONTDIRENTRY** para cada fonte no arquivo .res. Os aplicativos que geram arquivos .res com recursos de fonte também devem adicionar ao arquivo uma **estrutura FONTDIRENTRY** para cada fonte.

As declarações de fonte podem ser misturadas com outras declarações de recurso no . Arquivo RC porque as fontes não precisam ser contíguas no arquivo .res.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Recursos](resources.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

