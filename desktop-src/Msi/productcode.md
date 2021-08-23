---
description: A propriedade ProductCode é um identificador exclusivo para a versão específica do produto, representada como um GUID de cadeia de caracteres, por exemplo &\# 0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propriedade ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a77ba270075b214d5eee2ee804c6849a2ef71561610ee60ae3eb4941e43465c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753905"
---
# <a name="productcode-property"></a>Propriedade ProductCode

A propriedade **ProductCode** é um identificador exclusivo para a versão específica do produto, representada como um [GUID](guid.md)de cadeia de caracteres, por exemplo " {12345678-1234-1234-1234-123456789012} ". As letras usadas neste GUID devem estar em letras maiúsculas. Essa ID deve variar para diferentes versões e idiomas.

Uma atualização de produto que atualiza um produto em um produto totalmente novo também deve alterar o código do produto. As versões de 32 bits e 64 bits do pacote de um aplicativo devem ser atribuídas a códigos de produtos diferentes.

O **ProductCode** é anunciado como uma propriedade de produto e é o método principal de especificar o produto. Essa propriedade é necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




