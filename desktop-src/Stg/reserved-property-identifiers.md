---
title: Identificadores de propriedade reservados
description: Os identificadores de propriedade reservados não podem ser usados como identificadores de propriedade (ID). Qualquer identificador de propriedade (ID) pode ser usado, exceto 0, 1, e qualquer valor maior que, ou igual a, 0x80000000. Esses valores de identificador de propriedade são reservados para uso por aplicativos.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a16a8e232a31864a402b01033a829183105905c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454107"
---
# <a name="reserved-property-identifiers"></a>Identificadores de propriedade reservados

Os identificadores de propriedade reservados não podem ser usados como identificadores de propriedade (ID). Qualquer identificador de propriedade (ID) pode ser usado, exceto 0, 1, e qualquer valor maior que, ou igual a, 0x80000000. Esses valores de identificador de propriedade são reservados para uso por aplicativos.

A tabela a seguir lista as IDs de propriedade reservadas e a descrição da qual a ID de propriedade está reservada.



| ID de propriedade reservada | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Reservado para a criação de um dicionário opcional do [nome de exibição do conjunto de propriedades](property-set-display-name-dictionary.md). Isso permite que os usuários do conjunto de propriedades anexem significado às propriedades, além das fornecidas pelo indicador de tipo.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Reservado como um indicador da página de código (Windows) ou script (Macintosh) a ser usado ao interpretar as cadeias de caracteres no conjunto de propriedades.<br/> Todos os valores de cadeia de caracteres no conjunto de propriedades devem ser armazenados com a mesma página de código. O valor do sistema operacional de origem no cabeçalho do conjunto de Propriedades (PROPERTYSETHEADER::d wOSVer) determina se o indicador da página de código corresponde a uma página de código do Windows ou a um script do Macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Reservado como uma indicação da localidade para a qual o conjunto de propriedades é gravado.<br/> A localidade padrão para um conjunto de propriedades é a localidade padrão do sistema (padrão do sistema de localidade \_ \_ ). Para obter mais informações sobre \_ \_ o padrão do sistema de localidade, consulte APIs do Win32. O padrão é usado no caso de o indicador de localidade não existir no conjunto de propriedades.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Reservado como um indicador de comportamentos de conjunto de propriedades. Esse valor de ID de propriedade é um \_ UI4 VT e começa com um tipo de dados **DWORD** que contém o valor VT \_ UI4 seguido por um **DWORD** indicando o comportamento do conjunto de propriedades.<br/> Atualmente, o único bit nesse valor definido é o bit de ordem baixo (0x1). Se esse bit for definido, ele indica que os nomes do conjunto de propriedades, indicados pela ID de propriedade 0, devem ser considerados diferenciando maiúsculas de minúsculas. Se esse bit não estiver definido ou se a propriedade Behavior (ID 0x80000003) não existir, os nomes deverão ser considerados não diferenciando maiúsculas de minúsculas.<br/> |
| 0xFFFFFFFF           | Reservado para a conveniência da programação. Ele nunca deve aparecer em um conjunto de propriedades serializadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Os identificadores de propriedade com o conjunto de bits alto (ou seja, valores negativos) são reservados para uso futuro pela Microsoft.

Das propriedades reservadas, aquelas com valores de ID no intervalo 0x80000000 a 0xBFFFFFFF são consideradas somente leitura por implementações que não entendem seu significado. Por exemplo, se uma implementação não entender o significado da propriedade 0x80000000, ela deve permitir que essa propriedade seja lida, mas não gravada ou excluída. Essa implementação deve permitir que uma propriedade no intervalo 0xC0000000 para 0xFFFFFFFE seja lida, gravada ou excluída. A ID de propriedade 0xFFFFFFFF é um valor reservado e nunca deve aparecer em um conjunto de propriedades serializadas.

## <a name="property-set-locale"></a>Localidade do conjunto de propriedades

Os aplicativos podem optar por dar suporte à localidade ou usar o comportamento padrão. É recomendável que os aplicativos permitam que os usuários especifiquem uma localidade de trabalho. Esses aplicativos devem gravar o identificador de localidade especificado pelo usuário na propriedade. Os aplicativos que usam a localidade padrão do usuário (localidade do \_ usuário padrão \_ ) devem gravar o identificador de localidade padrão do usuário na propriedade. Para obter mais informações sobre \_ \_ o padrão de usuário de localidade, consulte a API do Win32.

> [!Note]  
> Se a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) for usada para criar um conjunto de propriedades, a localidade padrão do usuário será automaticamente gravada como o indicador de localidade.

 

Os aplicativos também devem lidar com o caso de um objeto estrangeiro, que é aquele em que a localidade não é a localidade do aplicativo, a localidade do usuário ou a localidade do sistema.

A propriedade de indicador de localidade é do tipo VT \_ U14 e, portanto, consiste em um **DWORD** que contém \_ o VT U14, seguido por um **DWORD** que contém o LCID (identificador de localidade), conforme definido na API do Win32.

## <a name="code-page-indicator"></a>Indicador de página de código

Quando um aplicativo que não é o autor de um conjunto de propriedades altera uma propriedade do tipo cadeia de caracteres no conjunto, ele deve examinar o indicador da página de código e executar uma das seguintes ações:

-   Escreva a cadeia de caracteres no formato especificado pelo indicador da página de código.
-   Substitua e reescreva para alterar a página de código.

Se um aplicativo não puder reconhecer esse indicador, ele não deverá modificar a propriedade. Todos os criadores de conjuntos de propriedades devem gravar um indicador de página de código; no entanto, se o indicador da página de código não estiver presente, a página de código predominante no computador do leitor deverá ser assumida.

> [!Note]  
> Se a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) for usada para criar um conjunto de propriedades, o indicador da página de código será gravado automaticamente.

 

Os valores possíveis para a página de código são fornecidos na API do Win32 (para obter mais informações, consulte a função [**GetACP**](/windows/desktop/api/winnls/nf-winnls-getacp) ) e *dentro do Macintosh volume VI*, páginas 14-111. (Esses recursos podem não estar disponíveis em alguns idiomas e países.) Por exemplo, a página de código em ANSI é representada por 0x04E4 (1252 em decimal) enquanto a página de código para Unicode é 0x04B0 (1200 em decimal).

É recomendável que a página de código Unicode seja usada quando possível e use o \_ LPWStr do VT em vez de VT \_ LPSTR para evitar conversões Unicode de < > de vários bytes durante o armazenamento e a recuperação. Usar a mesma página de código para todos os conjuntos de propriedades é a única maneira de atingir conjuntos de propriedades interoperáveis em todo o mundo. Na página de código Unicode ou não-Unicode, lembre-se de que a contagem no início de um VT \_ LPSTR ou VT \_ BSTR é uma contagem de **bytes** e não uma contagem de **caracteres** . Essa contagem de bytes inclui um ou dois bytes de zero no final da cadeia de caracteres (o terminador **nulo** da cadeia de caracteres).

A ID de propriedade 1 é um \_ tipo VT I2 e começa com um **DWORD** que contém o valor VT \_ i2 seguido por um **curto** que indica a página de código.

 

