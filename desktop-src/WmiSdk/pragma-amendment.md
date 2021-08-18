---
description: Direciona o compilador MOF para separar um arquivo MOF em versões específicas do idioma e neutras ao idioma.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: pragma amendment
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
ms.openlocfilehash: 6204ac7f3cd78de8d2eed9740fc165475d387e65284bcbf6be1ea10ed91a0926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992726"
---
# <a name="pragma-amendment"></a>pragma amendment

O **comando do pré-processador pragma amendment** direciona o compilador MOF para separar um arquivo MOF em versões específicas de idioma e neutras a idioma. O arquivo MOF específico do idioma move qualificadores corrigidos para um namespace para uma localidade específica. Em seguida, você compila os arquivos MOF específicos do idioma e neutros em idioma para armazenar informações de classe no repositório WMI.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como criar um arquivo MOF que contém qualificadores corrigidos. Em seguida, você pode compilar o código MOF com o seguinte comando:

**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**

O comando instrui o compilador MOF a produzir dois arquivos MOF do arquivo Mastermof.mof original. O compilador MOF produz uma versão neutra em idioma do arquivo MOF, chamada Lnmof.mof, com todos os itens específicos do idioma removidos. O compilador também cria um segundo arquivo MOF específico de linguagem chamado Lsmof.mfl que contém apenas itens que você deve localizado.

> [!Note]  
> Ao dividir um arquivo MOF com o qualificador **de** alteração ou o **comando pragma amendment,** você deve especificar as opções **-MOF** e **-MFL.** Caso contrário, o compilador não gerará nenhum arquivo de saída. Em seguida, você deve compilar os dois arquivos de saída para disponibilizar as informações de classe para o WMI.

 


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

 

 




