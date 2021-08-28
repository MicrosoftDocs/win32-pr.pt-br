---
title: Chave FileType
description: Usado por GetClassFile para corresponder padrões com vários bytes de arquivo em um arquivo não composto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Chave do Registro FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2899b69c2f433fbd3587bdd7baa6c17c4f8cc4c9cd32100dcd672f9d213d4d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462488"
---
# <a name="filetype-key"></a>Chave FileType

Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões com vários bytes de arquivo em um arquivo não composto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*Deslocamento*
</dt> <dd>

Determina a distância do início ou do fim do arquivo para iniciar a comparação. Se o deslocamento for um valor negativo, a comparação começará do final do arquivo menos o valor de deslocamento. O valor de deslocamento é um tipo decimal, a menos que precedido por "0x".

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Representa o comprimento em bytes do início ao final do arquivo. Representa o intervalo de byte no arquivo. O *valor cb* é um decimal, a menos que precedido por "0x".

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*Máscara*
</dt> <dd>

Um valor binário usado para mascaramento, que é executado usando uma operação AND lógica e o intervalo de byte especificado por *offset* e *cb*. Se esse valor for omitido, os bytes serão definidos como todos. Esse valor é sempre hexadecimal.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valor*
</dt> <dd>

Representa o padrão que deve corresponder a um arquivo desse tipo de arquivo. O padrão é usado para identificar corretamente um formato de arquivo conhecido de seu conteúdo, não por sua extensão.

</dd> </dl>

## <a name="remarks"></a>Comentários

As entradas são usadas pela [**função GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões a vários bytes de arquivo em um arquivo não composto. **FileType** tem subkeys CLSID, cada uma das quais tem uma série de subkeys **0**, **1**, **2**, **3**. Esses valores contêm padrões que, se um corresponde, produzir o CLSID indicado. Por exemplo, um valor de "0, 4, FFFFFFFF, ABCD1234" indica que os primeiros 4 bytes devem ser ABCD1234, nessa ordem. Um valor de "-4, 4, FEFEFEFE" indica que os últimos quatro bytes no arquivo devem ser FEFEFEFE. Se qualquer um dos padrões corresponde, o CLSID é retornado.

A **chave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde à chave **\_ \_ RAIZ de CLASSES HKEY,** que foi mantida para compatibilidade com versões anteriores do COM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**<extensão \_ de arquivo>**](-file-extension--key.md)
</dt> <dt>

[**Getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




