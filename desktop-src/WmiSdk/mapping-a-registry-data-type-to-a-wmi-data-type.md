---
description: O aplicativo deve criar as propriedades com um tipo de dados que é mapeado para o tipo de dados do registro.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Mapeando um tipo de dados do registro para um tipo de dados WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b96a3bcda0060e376427375059f006e3241118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506097"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Mapeando um tipo de dados do registro para um tipo de dados WMI

O aplicativo deve criar as propriedades com um tipo de dados que é mapeado para o tipo de dados do registro. Você não precisa especificar o tipo de dados do registro nos métodos que criam, obtêm ou definem valores de registro. No entanto, o parâmetro de entrada que contém o valor deve estar no tipo de dados correto do WMI. Por exemplo, se um aplicativo recebe dados **reg \_ DWORD** do registro, a classe que recebe os dados deve incluir uma propriedade **UInt32** .

A tabela a seguir lista o mapeamento entre os tipos de dados do registro e do WMI usados nos métodos [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) .



| Tipo de dados do registro      | Tipo de dados WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_binário reg**         | matriz **uint8**<br/> Uma matriz de valores que não excedem 255 ou FF Hex. Por exemplo, o código de script a seguir Visual Basic cria uma matriz que se adapta a esse tipo de dados.<br/> `BinArray = Array(&H01, &Ha2)`<br/> O método de classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) requer o tipo de dados **\_ Binary reg** .<br/>                                                                                          |
| **REG \_ DWORD**          | **UInt32**, **sint32** ou Visual Basic **inteiro**<br/> Um único valor de 32 bits. Os métodos de classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**getdwordvalue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) e [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) exigem o tipo de dados **reg \_ DWORD** .<br/>                                                                                                                                                                  |
| **REG \_ sz**             | **cadeia de caracteres**<br/> O método de classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) requer o tipo de dados **reg \_ sz** .<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **UInt64**.<br/> Um único valor de 64 bits. Os métodos da classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**getqwordvalue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) e [**setqwordvalue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) exigem o tipo de dados **reg \_ QWORD** .<br/>                                                                                                                                                                                                         |
| **REG \_ expande \_ sz**     | **cadeia de caracteres**<br/> As cadeias de caracteres expandidas são cadeias especiais que representam variáveis de ambiente do sistema. Por exemplo, o código VBScript a seguir cria uma cadeia de caracteres que representa a variável de ambiente de **\_ \_ usuário local hKey** Temp.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> O método de classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) requer o tipo de dados **reg \_ expande \_ sz** .<br/> |
| **REG \_ multi \_ sz**      | matriz de **cadeia de caracteres**<br/> O tipo de dados multistring contém várias cadeias de caracteres. Por exemplo, o código VBScript a seguir cria uma matriz que se adapta a esse tipo de dados.<br/> `MultiValue = Array("first", "second", "third")`<br/> O método de classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) requer o tipo de dados **reg \_ multi \_ sz** .<br/>                                                                     |
| **\_lista de recursos do reg \_** | Conforme apropriado. Para obter mais informações, consulte [descrevendo um recurso para o registro](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo classes para o provedor de registro do sistema](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

