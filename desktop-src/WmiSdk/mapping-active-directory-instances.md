---
description: Em geral, cada objeto de Active Directory é mapeado para exatamente uma instância do WMI.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Mapeando instâncias de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a3e40a6f4a85ebb1bb3d7e1e5a5de7bc43c754ff7672f694aff05b62853dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317633"
---
# <a name="mapping-active-directory-instances"></a>Mapeando instâncias de Active Directory

Em geral, cada objeto de Active Directory é mapeado para exatamente uma instância do WMI. A classe WMI correspondente à instância de WMI é a mesma que a classe fornecida pelo provedor de classe da classe de Active Directory correspondente. A propriedade de chave **ADSIPath** de cada instância é preenchida com o caminho ADSI do objeto.

As seções a seguir são discutidas neste tópico:

-   [Mapeando namespaces](#mapping-namespaces)
-   [Mapeando valores de atributo](#mapping-attribute-values)
-   [Mapeando associações de instância](#mapping-instance-associations)

> [!Note]  
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Mapeando namespaces

Cada um dos namespaces no ADSI mapeia um-para-um para namespaces no namespace do \\ diretório raiz do WMI \\ . O nome do namespace WMI é o mesmo que o valor **ProgID** do provedor de serviços de diretório que fornece o namespace. Especificamente, Active Directory mapeia para o \\ namespace LDAP no \\ namespace do \\ diretório raiz. O WMI cria o \\ namespace LDAP como parte do processo de registro do provedor de classe.

## <a name="mapping-attribute-values"></a>Mapeando valores de atributo

A tabela a seguir lista o mapeamento entre cada atributo de um Active Directory objeto e uma propriedade WMI.



| Sintaxe de Active Directory | Tipo de dados WMI                                 | Valor da propriedade WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Boolean                 | **\_booliano de CIM**                              | Mapeado diretamente para o valor booliano apropriado.                         |
| Cadeia de caracteres sem diferenciação de maiúsculas | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Cadeia de caracteres diferencia maiúsculas de minúscula   | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Nome Distinto      | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| DN-Binary               | Objeto inserido de DN de classe **\_ com \_ binário** | Mapeado para instâncias do **DN com classe de \_ cadeia de \_ caracteres** .                    |
| DN-String               | Objeto inserido de DN de classe **\_ com \_ cadeia de caracteres** | Mapeado para instâncias do **DN com classe de \_ cadeia de \_ caracteres** .                    |
| Enumeração             | **\_Sint32 CIM**                               | Mapeado diretamente para o valor inteiro.                                     |
| IA5-String              | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Integer                 | **\_Sint32 CIM**                               | Mapeado diretamente para o valor inteiro.                                     |
| Descritor de segurança NT  | Objeto inserido da classe **Uint8Array**       | Mapeado para instâncias da classe **Uint8Array** .                          |
| Cadeia de caracteres numérica          | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| ID do objeto               | **\_cadeia de caracteres CIM**                               | Mapeado da representação de cadeia de caracteres da OID; por exemplo, "1.3.3.4". |
| Cadeia de caracteres de octeto            | Objeto inserido da classe **Uint8Array**       | Mapeado para instâncias da classe **Uint8Array** .                          |
| OU nome                 | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Presentation-Address    | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Imprimir cadeia de caracteres de caso       | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Link de réplica            | Objeto inserido da classe **Uint8Array**       | Mapeado para instâncias da classe **Uint8Array** .                          |
| SID                     | Objeto inserido da classe **Uint8Array**       | Mapeado para instâncias da classe **Uint8Array** .                          |
| Tempo                    | **\_data e hora CIM**                             | Convertido na representação de \_ data e hora CIM e mapeado.                 |
| Indefinido               | N/D                                           | N/D                                                                       |
| Cadeia de caracteres Unicode          | **\_cadeia de caracteres CIM**                               | Mapeado a partir do valor da cadeia de caracteres.                                      |
| Hora codificada UTC          | **\_data e hora CIM**                             | Convertido na representação de \_ data e hora CIM e mapeado.                 |



 

Para obter mais informações sobre **Uint8Array** e **DN \_ com \_ Binary**, consulte [Mapping Attributes](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Mapeando associações de instância

O provedor de serviços de diretório mapeia as diferentes relações de contêiner em Active Directory usando instâncias da classe de [**\_ \_ \_ contenção de instância LDAP do DS**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) .

 

 
