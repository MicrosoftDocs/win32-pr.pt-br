---
description: A propriedade ProductLanguage especifica o idioma que o instalador deve usar para todas as cadeias de caracteres na interface do usuário que não são criadas no banco de dados.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propriedade ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792491"
---
# <a name="productlanguage-property"></a>Propriedade ProductLanguage

A propriedade **ProductLanguage** especifica o idioma que o instalador deve usar para todas as cadeias de caracteres na interface do usuário que não são criadas no banco de dados. Essa propriedade deve ser um identificador de idioma numérico (LANGid). Se uma transformação alterar o idioma da interface do usuário no banco de dados, ela também deverá alterar o valor dessa propriedade para refletir a nova linguagem.

Essa propriedade é necessária.

## <a name="remarks"></a>Comentários

O valor da propriedade **ProductLanguage** deve ser um dos idiomas listados na propriedade Summary do [**modelo**](template-summary.md) .

Ao criar um pacote como com neutralidade de idioma, defina a propriedade **ProductLanguage** como 0 e use a fonte MS Shell Dlg como o estilo de texto para todas as caixas de diálogo criadas. Como algumas fontes não dão suporte a todos os conjuntos de caracteres, usando essa fonte, você pode garantir que o texto seja exibido corretamente em todas as versões localizadas do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




