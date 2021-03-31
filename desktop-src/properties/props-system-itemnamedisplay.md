---
description: O nome de exibição no &\# 0034; mais completo&\# 0034; Form.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647552"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

O nome de exibição no formulário "mais completo". É a representação exclusiva do nome do item mais apropriada para os usuários finais.

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

Os valores de PKEY são definidos em Propkey. h.

Esse valor é o concatentation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md).

Se o item for um arquivo, essa propriedade incluirá o nome de exibição, conforme mostrado no explorador de arquivos. Há casos aceitáveis quando [System. FileName](./props-system-filename.md) é fornecido, mas o valor dessa propriedade é completamente diferente. As mensagens de email são um bom exemplo. Se o item for uma mensagem de email, o nome do item normalmente será o assunto. Nesse caso, o valor deve ser a concatenação de [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md). Como o valor de System. ItemNamePrefix exclui espaços à direita, a concatenação deve incluir um espaço ao gerar [System. ItemNameDisplay](). Observe que essa propriedade não tem garantia de ser exclusiva, mas foi projetada para promover o candidato mais provável que pode ser exclusivo e também faz sentido para os usuários finais.

Por exemplo, para documentos, o [System. title](./props-system-title.md) pode ser usado como [System. ItemNameDisplay](), mas na prática o título dos documentos pode não ser útil ou exclusivo o suficiente para funcionar como o único System. ItemNameDisplay. Em vez disso, fornecer [System. FileName](./props-system-filename.md) como o valor de System. ItemNameDisplay é uma opção melhor. No Windows Mail, o email é armazenado no sistema de arquivos como arquivos. eml. Os valores de System. FileName para esses arquivos não são amigáveis para o homem, pois são GUIDs. Neste exemplo, promover [System. Subject](./props-system-subject.md) como System. ItemNameDisplay faz mais sentido.

**Notas de compatibilidade:**

-   Implementações de pastas do Shell no Windows Vista: Use PKEY \_ ItemNameDisplay para a coluna nome quando desejar que o Windows Explorer chame [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ normal) para obter o valor do nome. Use outro PKEY, como PKEY \_ ItemName, quando você quiser que o Windows Explorer chame o repositório de propriedades da pasta ou [**IShellFolder2:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) para obter o valor do nome.
-   Implementações de pastas do Shell no Windows XP: a primeira coluna deve ser a coluna Name e o Windows Explorer chama [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para obter o valor do nome. O PKEY/SCID não importa.



| Tipo de item     | Exemplo                   |
|---------------|---------------------------|
| Arquivo          | olá.txt                 |
| Mensagem       | Re: onde está a reunião? |
| Pasta do dispositivo | Song. WMA                  |
| Pasta        | Documentos                 |



 

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
</dt> </dl>

 

 
