---
title: Identificadores de propriedade reservada
description: Identificadores de propriedade reservada não podem ser usados como identificadores de propriedade (ID). Qualquer ID (identificador de propriedade) pode ser usado, exceto 0, 1 e qualquer valor maior ou igual a, 0x80000000. Esses valores de identificador de propriedade são reservados para uso por aplicativos.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05053fd2a31a5e8ceec63420e74884484abef12d44dcfe3e7023c81b5e67e27a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683056"
---
# <a name="reserved-property-identifiers"></a>Identificadores de propriedade reservada

Identificadores de propriedade reservada não podem ser usados como identificadores de propriedade (ID). Qualquer ID (identificador de propriedade) pode ser usado, exceto 0, 1 e qualquer valor maior ou igual a, 0x80000000. Esses valores de identificador de propriedade são reservados para uso por aplicativos.

A tabela a seguir lista as IDs de propriedade reservada e a descrição para a qual a ID da propriedade está reservada.



| ID da propriedade reservada | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Reservado para criar um dicionário de nome de exibição de conjunto [de propriedades opcional.](property-set-display-name-dictionary.md) Isso permite que os usuários do conjunto de propriedades anexem o significado às propriedades, além daquelas fornecidas pelo indicador de tipo.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Reservado como um indicador da página de código (Windows) ou Script (Macintosh) a ser usado ao interpretar as cadeias de caracteres no conjunto de propriedades.<br/> Todos os valores de cadeia de caracteres no conjunto de propriedades devem ser armazenados com a mesma página de código. O valor do sistema operacional de origem no header do conjunto de propriedades (PROPERTYSETHEADER::d wOSVer) determina se o indicador de página de código corresponde a uma página de código Windows ou script Macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Reservado como uma indicação da localidade para a qual o conjunto de propriedades é gravado.<br/> A localidade padrão de um conjunto de propriedades é a localidade padrão do sistema (LOCALE \_ SYSTEM \_ DEFAULT). Para obter mais informações sobre LOCALE \_ SYSTEM \_ DEFAULT, consulte as APIs do Win32. O padrão é usado no caso de o indicador de localidade não existir no conjunto de propriedades.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Reservado como um indicador de comportamentos do conjunto de propriedades. Esse valor de ID de propriedade é uma UI4 VT e começa com um tipo de dados DWORD que contém o valor \_ VT UI4 seguido por um  \_ **DWORD** que indica o comportamento do conjunto de propriedades.<br/> Atualmente, o único bit nesse valor definido é o bit de ordem baixa (0x1). Se esse bit estiver definido, ele indicará que os nomes de conjunto de propriedades, indicados pela ID da propriedade 0, devem ser considerados com valor de minúsculas. Se esse bit não estiver definido ou se a propriedade de comportamento (ID 0x80000003) não existir, os nomes deverão ser considerados sem maiúsculas e minúsculas.<br/> |
| 0xFFFFFFFF           | Reservado para a conveniência da programação. Ele nunca deve aparecer em um conjunto de propriedades serializado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Identificadores de propriedade com o conjunto de bits alto (ou seja, valores negativos) são reservados para uso futuro pela Microsoft.

Das propriedades reservadas, aquelas com valores de ID no intervalo 0x80000000 a 0xBFFFFFFF são consideradas somente leitura por implementações que não entendem seu significado. Por exemplo, se uma implementação não entender o significado da propriedade 0x80000000, ela deverá permitir que essa propriedade seja lida, mas não escrita ou excluída. Essa implementação deve permitir que uma propriedade no intervalo 0xC0000000 0xFFFFFFFE ser lida, escrita ou excluída. A ID da 0xFFFFFFFF é um valor reservado e nunca deve aparecer em um conjunto de propriedades serializado.

## <a name="property-set-locale"></a>Localidade do conjunto de propriedades

Os aplicativos podem optar por dar suporte à localidade ou usar o comportamento padrão. É recomendável que os aplicativos permitam que os usuários especifiquem uma localidade em funcionamento. Esses aplicativos devem gravar o identificador de localidade especificado pelo usuário na propriedade . Os aplicativos que usam a localidade padrão do usuário (LOCALE USER DEFAULT) devem gravar o identificador de localidade \_ padrão do usuário na propriedade \_ . Para obter mais informações sobre LOCALE \_ USER \_ DEFAULT, consulte a API do Win32.

> [!Note]  
> Se a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) for usada para criar um conjunto de propriedades, a localidade padrão do usuário será escrita automaticamente como o Indicador de Localidade.

 

Os aplicativos também devem lidar com o caso de um objeto externo, que é aquele em que a localidade não é a localidade do aplicativo, a localidade do usuário ou a localidade do sistema.

A propriedade do indicador de localidade é do tipo VT U14 e, portanto, consiste em uma DWORD que contém a VT U14, seguida por uma DWORD que contém o LCID (Identificador de Localidade), conforme definido na \_ API do  \_ Win32. 

## <a name="code-page-indicator"></a>Indicador de página de código

Quando um aplicativo que não é o autor de um conjunto de propriedades altera uma propriedade do tipo cadeia de caracteres no conjunto, ele deve examinar o indicador de página de código e tomar uma das seguintes ações:

-   Escreva a cadeia de caracteres no formato especificado pelo indicador de página de código.
-   Substitua e reescreva para alterar a página de código.

Se um aplicativo não puder reconhecer esse indicador, ele não deverá modificar a propriedade . Todos os criadores de conjuntos de propriedades devem escrever um indicador de página de código; no entanto, se o indicador de página de código não estiver presente, a página de código predominante no computador do leitor deverá ser assumida.

> [!Note]  
> Se a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) for usada para criar um conjunto de propriedades, o indicador de página de código será gravado automaticamente.

 

Os valores possíveis para a página de código são dados na API do Win32 (para obter mais informações, consulte a função [**GetACP)**](/windows/desktop/api/winnls/nf-winnls-getacp) e *Dentro do Volume VI do Macintosh,* páginas 14-111. (Esses recursos podem não estar disponíveis em alguns idiomas e países.) Por exemplo, a página de código US ANSI é representada por 0x04E4 (1252 em decimal), enquanto a página de código para Unicode é 0x04B0 (1200 em decimal).

É recomendável que a página de código Unicode seja usada quando possível e use vT LPWSTR em vez de VT LPSTR para evitar conversões Unicode <-> multibyte durante o armazenamento e \_ \_ a recuperação. Usar a mesma página de código para todos os conjuntos de propriedades é a única maneira de obter conjuntos de propriedades interoperáveis em todo o mundo. Na página de código Unicode ou não Unicode, esteja ciente de que a contagem no início de um VT LPSTR ou BSTR VT é uma contagem de byte e não uma contagem de \_ \_ caracteres.   Essa contagem de bytes inclui um ou dois bytes zero no final da cadeia de caracteres (o terminador **NULL** da cadeia de caracteres).

A ID da propriedade 1 é um tipo VT I2 e começa com um DWORD que contém o valor VT I2 seguido por um SHORT que indica \_ a página de  \_ código. 

 

