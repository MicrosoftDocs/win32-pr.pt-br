---
description: O tipo canônico do item.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171564"
---
# <a name="systemitemtype"></a>System. ItemType

O tipo canônico do item.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

O valor de System. ItemType deve ser analisado programaticamente e pode ser:

-   Uma extensão de arquivo que aponta para um valor de ProgID ( \_ raiz de classes hKey) que \_ \\ <ProgID> mantém o nome de exibição do tipo.
-   Um valor ProgID (HKEY \_ classes \_ RROOT \\ <ProgID> ), que contém o nome de exibição do tipo.

O elemento FriendlyTypeName de um ProgID deve ser uma versão localizada do nome do aplicativo ( @winword.dll ,-42), enquanto o valor padrão da chave ProgID é um nome não localizado (Word.Document. 12).

Se não houver nenhum tipo canônico, o valor será VT \_ vazio. Se o item for um arquivo ([System. FileName](./props-system-filename.md) não for VT \_ Empty), o valor será o mesmo que [System. FileExtension](./props-system-fileextension.md). Use [System. ItemTypeText](./props-system-itemtypetext.md) quando desejar exibir o tipo para usuários finais em uma exibição.

> [!Note]  
> Se o item for um arquivo, passar o valor de [System. ItemType]() para [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) resultará no mesmo valor que [System. ItemTypeText](./props-system-itemtypetext.md).

 

Valores de exemplo:



| Caminho                                   | ItemType         |
|----------------------------------------|------------------|
| c: \\ barra de mydir \\ \\hello.txt              | .txt             |
| \\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc | .doc             |
| \\\\\\pasta de compartilhamento do servidor \\              | Diretório        |
| c: \\ mydir \\ MyFolder                    | Diretório        |
| \[desktop\]                            | Pasta           |
| /Mailbox conta/caixa de entrada/' re: Olá! '    | MAPI/IPM. Mensagem |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[Identificadores programáticos](../shell/fa-progids.md)
</dt> </dl>

 

 
