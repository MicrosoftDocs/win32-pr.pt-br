---
description: Você deve compilar o arquivo MOF mestre para criar os arquivos MOF de idioma neutro e específico do idioma.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilando arquivos MOF localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d23c77fee8a745b6032848c124a24ffb8e7cf626b0ff3c87fecc7e05b14d372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556795"
---
# <a name="compiling-localized-mof-files"></a>Compilando arquivos MOF localizados

Você deve compilar o arquivo MOF mestre para criar os arquivos MOF de idioma neutro e específico do idioma.

Digite o comando a seguir em um prompt de comando para compilar um arquivo MOF mestre.

**Mofcomp-MOF: Lnmof. mof-MFL: Lsmof. MFL-emenda: MS \_ 409 Mastermof. mof**

Quando você executa esse comando, o compilador MOF cria dois arquivos MOF do arquivo original Mastermof. mof. O compilador MOF produz uma versão neutra de idioma, Lnmof. MOF, na qual todos os itens específicos do idioma são removidos. Uma segunda versão específica de idioma, Lsmof. MOF, também é criada; Esse arquivo contém apenas os itens que foram marcados com o tipo de qualificador [**corrigido**](qualifier-flavors.md) no arquivo Mastermof. mof.

O exemplo de código a seguir mostra o conteúdo do arquivo MOF neutro de idioma (Lnmof. MOF) que é gerado.

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

O exemplo de código a seguir mostra o conteúdo do arquivo MOF específico do idioma (Lsmof. MFL) que é gerado.

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

A compilação de um arquivo MOF com o qualificador [**corrigido**](qualifier-flavors.md) gera apenas arquivos MOF separados por idiomas e idiomas específicos. o repositório CIM não é atualizado com as novas informações de classe. Você deve usar o compilador MOF para compilar os dois arquivos MOF que a primeira compilação produziu antes que qualquer informação de classe esteja disponível para o WMI.

Quando você compila um arquivo MOF mestre, somente os qualificadores com o tipo [**emendado**](qualifier-flavors.md) são movidos para o arquivo MOF específico do idioma. Os qualificadores que não têm o tipo **emendado** não são localizados e só existem na definição de classe básica no arquivo MOF com neutralidade de idioma. Qualificadores não-locais podem ser usados para descrições padrão se as descrições localizadas não estiverem disponíveis.

Você pode usar o comando de [alteração de pragma](pragma-amendment.md) em vez de especificar [**emendado**](qualifier-flavors.md) como uma opção para o compilador MOF. Qualquer uma dessas opções é equivalente a solicitar versões específicas do idioma e de idioma neutro de um arquivo MOF. Se você usar o comando de alteração de pragma ou a opção de linha de comando **corrigida** , deverá especificar o nome dos arquivos de saída usando as opções **-MFL** e **-MOF** no prompt de comando.

> [!Note]  
> O arquivo MOF com neutralidade de idioma gerado pelo compilador MOF contém o equivalente Decimal da ID de localidade, mesmo que esse valor tenha sido inserido em hexadecimal. No exemplo acima, o compilador converteu o valor 0x409 para o número decimal 1033 para o arquivo de saída Lnmof. mof.

 

 

 



