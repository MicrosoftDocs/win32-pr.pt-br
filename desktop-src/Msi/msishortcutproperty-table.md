---
description: A tabela MsiShortcutProperty permite que o instalador de janela defina propriedades para atalhos que também são objetos de shell do Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabela MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506109"
---
# <a name="msishortcutproperty-table"></a>Tabela MsiShortcutProperty

A tabela MsiShortcutProperty permite que o instalador de janela defina propriedades para atalhos que também são objetos de [shell do Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . A partir do Windows Vista e do Windows Server 2008, o Shell do Windows fornece uma interface IPropertyStore para objetos do Shell, como atalhos. Um pacote Windows Installer 5,0 em execução no Windows Server 2008 R2 ou no Windows 7 pode definir essas propriedades quando o atalho é instalado.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esta tabela está disponível a partir do Windows Installer 5,0.

A tabela MsiShortcutProperty tem as colunas a seguir.



| Coluna              | Tipo                         | Chave | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identificador](identifier.md) | S   | N        |
| Atalho\_          | [Identificador](identifier.md) | N   | N        |
| PropertyKey         | [Binário](formatted.md)   | N   | N        |
| PropVariantValue    | [Binário](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

Identificador exclusivo desta linha da tabela MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Atalho\_
</dt> <dd>

Uma chave na tabela de [atalho](shortcut-table.md) que identifica o atalho com uma propriedade definida.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Um valor de cadeia de caracteres que fornece informações para a estrutura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . As informações neste campo devem se referir ao nome canônico de uma propriedade registrada com o sistema de propriedades do Windows. Para obter mais informações sobre o sistema de propriedades do Windows, consulte [visão geral do sistema de propriedades](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Um valor de cadeia de caracteres que fornece informações para a estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

Várias propriedades podem ser definidas em um atalho. Se a mesma propriedade for definida várias vezes no mesmo atalho, o valor será definido em uma ordem não especificada.

Windows Installer pode definir propriedades de atalho somente quando o atalho é instalado ou reinstalado. Um patch que não reinstala um atalho que já foi instalado não atualiza as propriedades do atalho. Um patch pode atualizar as propriedades, incluindo uma tabela de [atalho](shortcut-table.md) no pacote de patch e reinstalando o atalho.

## <a name="remarks"></a>Comentários

[Windows Installer mensagem de erro](windows-installer-error-messages.md) 1946 é retornada como um aviso e a instalação continuará, se Windows Installer não puder definir uma propriedade de atalho especificada na tabela MsiShortcutProperty.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
</dl>

 

 
