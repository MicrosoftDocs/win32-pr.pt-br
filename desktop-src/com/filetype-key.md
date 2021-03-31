---
title: Chave FileType
description: Usado por GetClassFile para corresponder padrões em vários bytes de arquivo em um arquivo não composto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Chave do registro de FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006084"
---
# <a name="filetype-key"></a>Chave FileType

Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões em vários bytes de arquivo em um arquivo não composto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*desvio*
</dt> <dd>

Determina a distância do início ou do fim do arquivo para iniciar a comparação. Se o deslocamento for um valor negativo, a comparação começará no final do arquivo menos o valor de deslocamento. O valor de deslocamento é um tipo decimal, a menos que seja precedido por "0x".

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Representa o comprimento em bytes desde o início até o fim do arquivo. Representa o intervalo de bytes no arquivo. O valor *CB* é um decimal, a menos que seja precedido por "0x".

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*mascara*
</dt> <dd>

Um valor binário usado para mascaramento, que é executado usando uma operação AND lógica e o intervalo de bytes especificado por *offset* e *CB*. Se esse valor for omitido, os bytes serão definidos como todos. Esse valor é sempre hexadecimal.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Representa o padrão que deve corresponder a um arquivo para ser desse tipo de arquivo. O padrão é usado para identificar corretamente um formato de arquivo conhecido de seu conteúdo, não por sua extensão.

</dd> </dl>

## <a name="remarks"></a>Comentários

As entradas são usadas pela função [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões em vários bytes de arquivo em um arquivo não composto. O **filetype** tem subchaves CLSID, cada uma com uma série de subchaves **0**, **1**, **2**, **3**. Esses valores contêm padrões que, se houver correspondência, produzirão o CLSID indicado. Por exemplo, um valor de "0, 4, FFFFFFFF, ABCD1234" indica que os primeiros 4 bytes devem ser ABCD1234, nessa ordem. Um valor de "-4, 4, FEFEFEFE" indica que os últimos quatro bytes no arquivo devem ser FEFEFEFE. Se qualquer um dos padrões corresponder, o CLSID será retornado.

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**><\_ extensão de arquivo**](-file-extension--key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




