---
description: Direciona o compilador MOF para separar um arquivo MOF em versões de idioma neutros e específicas de idiomas.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: alteração de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647699"
---
# <a name="pragma-amendment"></a>alteração de pragma

O comando de pré-processador de **alteração de pragma** direciona o compilador MOF para separar um arquivo MOF em versões de idioma neutros e específicas de idiomas. O arquivo MOF específico do idioma move os qualificadores corrigidos para um namespace para uma localidade específica. Em seguida, você compila os arquivos MOF específicos do idioma e do idioma neutro para armazenar informações de classe no repositório do WMI.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como criar um arquivo MOF que contém qualificadores corrigidos. Em seguida, você pode compilar o código MOF com o seguinte comando:

**Mofcomp** **-MOF: Lnmof. mof** **-MFL: Lsmof. MFL** **Mastermof. mof**

O comando instrui o compilador MOF a produzir dois arquivos MOF do arquivo original Mastermof. mof. O compilador MOF produz uma versão neutra de idioma do arquivo MOF, chamada Lnmof. MOF, com todos os itens específicos do idioma removidos. O compilador também cria um segundo arquivo MOF específico de idioma chamado Lsmof. MFL que contém apenas os itens que você deve localizar.

> [!Note]  
> Ao dividir um arquivo MOF com o qualificador de **emenda** ou o comando de **alteração de pragma** , você deve especificar as opções **-MOF** e **-MFL** . Caso contrário, o compilador não gerará nenhum arquivo de saída. Em seguida, você deve compilar os dois arquivos de saída para disponibilizar as informações de classe para o WMI.

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 




