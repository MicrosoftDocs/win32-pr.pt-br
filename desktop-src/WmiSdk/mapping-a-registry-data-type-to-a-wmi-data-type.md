---
description: O aplicativo deve criar as propriedades com um tipo de dados que mapeia para o tipo de dados do Registro.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Mapeando um tipo de dados do Registro para um tipo de dados WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e620d51eee52592df946e822165d8ed1833214c6f75519d4274b0d7fe3f5550c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050684"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Mapeando um tipo de dados do Registro para um tipo de dados WMI

O aplicativo deve criar as propriedades com um tipo de dados que mapeia para o tipo de dados do Registro. Você não precisa especificar o tipo de dados do Registro nos métodos que criam, obterão ou definirão valores do Registro. No entanto, o parâmetro de entrada que contém o valor deve estar no tipo de dados WMI correto. Por exemplo, se um aplicativo receber dados **\_ REG DWORD** do Registro, a classe que recebe os dados deverá incluir uma **propriedade Uint32.**

A tabela a seguir lista o mapeamento entre os tipos de dados registry e WMI usados [**nos métodos StdRegProv.**](/previous-versions/windows/desktop/regprov/stdregprov)



| Tipo de dados do Registro      | Tipo de dados WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG \_ BINARY**         | **Matriz uint8**<br/> Uma matriz de valores que não excedem 255 ou hexa FF. Por exemplo, o código Visual Basic Script a seguir cria uma matriz que se ajusta a esse tipo de dados.<br/> `BinArray = Array(&H01, &Ha2)`<br/> O [**método de classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) requer o tipo de dados **REG \_ BINARY.**<br/>                                                                                          |
| **REG \_ DWORD**          | **uint32**, **sint32** ou Visual Basic **inteiro**<br/> Um único valor de 32 bits. Os [**métodos de classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) e [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) exigem o tipo de dados **REG \_ DWORD.**<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **cadeia de caracteres**<br/> O [**método de classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) requer o **tipo de dados REG \_ SZ.**<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **uint64**.<br/> Um único valor de 64 bits. Os [**métodos de classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) e [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) exigem o tipo de dados **REG \_ QWORD.**<br/>                                                                                                                                                                                                         |
| **REG \_ EXPAND \_ SZ**     | **cadeia de caracteres**<br/> Cadeias de caracteres expandidas são cadeias de caracteres especiais que representam variáveis de ambiente do sistema. Por exemplo, o código VBScript a seguir cria uma cadeia de caracteres que representa a variável de ambiente **TEMP HKEY \_ LOCAL \_ USER.**<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> O [**método de classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) requer o tipo de dados **REG EXPAND \_ \_ SZ.**<br/> |
| **REG \_ MULTI \_ SZ**      | **matriz de cadeia de** caracteres<br/> O tipo de dados Multistring contém várias cadeias de caracteres. Por exemplo, o código VBScript a seguir cria uma matriz que se ajusta a esse tipo de dados.<br/> `MultiValue = Array("first", "second", "third")`<br/> O [**método de classe StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) requer o tipo de **dados REG MULTI \_ \_ SZ.**<br/>                                                                     |
| **LISTA DE \_ RECURSOS REG \_** | Conforme apropriado. Para obter mais informações, [consulte Descrevendo um recurso para o Registro](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo classes para o provedor de registro do sistema](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

