---
description: O nome de exibição &\# 0034;mais completo&\# 0034; formulário.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34e21c0ded147789cadccc99aaf9b2a1910398430419edacc498214c6489d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598466"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

O nome de exibição no formulário "mais completo". É a representação exclusiva do nome do item mais apropriado para os usuários finais.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

Esse valor é a concatenação de [System.ItemNamePrefix](./props-system-itemnameprefix.md) e [System.ItemName](./props-system-itemname.md).

Se o item for um arquivo, essa propriedade incluirá o nome de exibição, conforme mostrado em Explorador de Arquivos. Há casos aceitáveis quando [System.FileName](./props-system-filename.md) é dado, mas o valor dessa propriedade é completamente diferente. Mensagens de email são um bom exemplo. Se o item for uma mensagem de email, o nome do item normalmente será o assunto. Nesse caso, o valor deve ser a concatenação de [System.ItemNamePrefix](./props-system-itemnameprefix.md) e [System.ItemName](./props-system-itemname.md). Como o valor de System.ItemNamePrefix exclui espaços à frente, a concatenação deve incluir um espaço ao gerar [System.ItemNameDisplay.]() Observe que essa propriedade não tem garantia de ser exclusiva, mas foi projetada para promover o candidato mais provável que pode ser exclusivo e também faz sentido para os usuários finais.

Por exemplo, para documentos, [o System.Title](./props-system-title.md) pode ser usado como [System.ItemNameDisplay,]()mas, na prática, o título dos documentos pode não ser útil ou exclusivo o suficiente para funcionar como o único System.ItemNameDisplay. Em vez disso, [fornecer System.FileName](./props-system-filename.md) como o valor de System.ItemNameDisplay é uma opção melhor. No Windows Mail, o email é armazenado no sistema de arquivos como arquivos .eml. Os valores de System.FileName para esses arquivos não são amigáveis para humanos, pois são GUIDs. Neste exemplo, promover [System.Subject](./props-system-subject.md) como System.ItemNameDisplay faz mais sentido.

**Notas de compatibilidade:**

-   Implementações de pasta do shell no Windows Vista: use PKEY ItemNameDisplay para a coluna name quando quiser que o Windows Explorer chame \_ [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN NORMAL) para obter o valor do \_ nome. Use outra PKEY, como PKEY ItemName, quando quiser que o Windows Explorer chame o armazenamento de propriedades da pasta ou \_ [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) para obter o valor do nome.
-   Implementações de pasta do shell no Windows XP: a primeira coluna deve ser a coluna name e o Windows Explorer chama [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para obter o valor do nome. O PKEY/SCID não importa.



| Tipo de item     | Exemplo                   |
|---------------|---------------------------|
| Arquivo          | olá.txt                 |
| Mensagem       | Re: Onde está a reunião? |
| Pasta do dispositivo | song.wma                  |
| Pasta        | Documentos                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
