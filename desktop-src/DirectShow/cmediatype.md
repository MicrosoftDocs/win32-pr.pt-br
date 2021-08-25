---
description: A classe CMediaType gerencia tipos de mídia. Essa classe herda a estrutura AM \_ MEDIA \_ TYPE. Ela pode ser lançada em uma variável do tipo AM \_ MEDIA \_ TYPE.
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Classe CMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49680848fc764cdbbdfeaf3bea363f29427a745297ef4fb39bca09159aa582f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831937"
---
# <a name="cmediatype-class"></a>Classe CMediaType

![Hierarquia de classes cmediatype](images/mtype01.png)

A `CMediaType` classe gerencia tipos de mídia. Essa classe herda a [**estrutura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Ele pode ser lançado em uma variável do tipo **AM \_ MEDIA \_ TYPE**.



| Métodos públicos                                                      | Descrição                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Cmediatype**](cmediatype-cmediatype.md)                         | Método do construtor.                                                            |
| [**~CMediaType**](cmediatype--cmediatype.md)                       | Método destruidor.                                                             |
| [**Definir**](cmediatype-set.md)                                       | Define o tipo de mídia de outro tipo de mídia.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Determina se um tipo principal foi atribuído a esse objeto.              |
| [**Tipo**](cmediatype-type.md)                                     | Recupera o tipo principal.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Especifica o tipo principal.                                                      |
| [**Subtipo**](cmediatype-subtype.md)                               | Recupera o subtipo .                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Especifica o subtipo .                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Determina se os exemplos têm um tamanho fixo ou um tamanho variável.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Determina se o fluxo usa compactação temporal.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Recupera o tamanho da amostra.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Especifica um tamanho de exemplo fixo ou especifica que os exemplos têm um tamanho variável. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Especifica que os exemplos não têm um tamanho fixo.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Especifica se os exemplos são compactados usando compactação temporal.           |
| [**Formatar**](cmediatype-format.md)                                 | Recupera um ponteiro para o bloco de formato.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Recupera o comprimento do bloco de formato.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Especifica o tipo do formato.                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Recupera o tipo de formato.                                                     |
| [**Setformat**](cmediatype-setformat.md)                           | Especifica o bloco de formato.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Exclui o bloco de formato.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Aloca memória para o bloco de formato.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Relocar o bloco de formato para um novo tamanho.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Inicializa o tipo de mídia.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Determina se o tipo de mídia está parcialmente definido.                             |
| Operadores                                                           | Descrição                                                                    |
| [**operator =**](cmediatype-operator-.md)                          | Sobrecarrega o operador de atribuição para copiar um tipo de mídia.                        |
| [**operator ==**](cmediatype-operator--.md)                        | Testa a igualdade entre objetos `CMediaType`.                               |
| [**operator !=**](cmediatype-operator-neq.md)                      | Testa a desigualdade entre objetos `CMediaType`.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




