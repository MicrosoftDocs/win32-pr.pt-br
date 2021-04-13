---
title: Recurso de BITMAP
description: Define um bitmap que um aplicativo usa na tela de exibição ou como um item em um menu ou controle.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menus de recursos de BITMAP e outros recursos
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365908"
---
# <a name="bitmap-resource"></a>Recurso de BITMAP

Define um bitmap que um aplicativo usa na tela de exibição ou como um item em um menu ou controle.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Nome do arquivo que contém o recurso. O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual. O caminho deve ser uma cadeia de caracteres entre aspas.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define dois recursos de bitmap:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando bitmaps](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 