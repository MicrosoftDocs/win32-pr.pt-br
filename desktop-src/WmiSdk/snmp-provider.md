---
description: O provedor SNMP (Simple Network Management Protocol) permite que aplicativos cliente acessem informações de SNMP por meio de Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI e SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171977"
---
# <a name="wmi-and-snmp"></a>WMI e SNMP

O provedor SNMP (Simple Network Management Protocol) permite que aplicativos cliente acessem informações de SNMP por meio de Instrumentação de Gerenciamento do Windows (WMI). O provedor SNMP não é instalado por padrão. Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

O SNMP (Simple Network Management Protocol) usa um esquema para definir objetos. O esquema é diferente do esquema usado no WMI. O esquema SNMPv1 e SNMPv2C é chamado de estrutura de informações de gerenciamento (SMI) e é empacotado como arquivos de MIB (base de informações de gerenciamento). Os arquivos MIB definem objetos usando uma linguagem padrão — o ASN. 1) — e várias definições de macro que servem como modelos para descrever os objetos. As macros fornecem informações como o nome do objeto, o identificador, a sintaxe, a descrição, os direitos de acesso, as operações de protocolo e a codificação de protocolo. A tabela a seguir lista como o provedor SNMP trata diferentes aspectos de um objeto MIB.



| Tópico                                                    | Descrição                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [Macro do tipo de notificação](notification-type-macro.md)   | Como a macro do **tipo de notificação** é MAPEADA de SNMP para WMI.  |
| [Macro de tipo de objeto](object-type-macro.md)               | Como a macro do **tipo de objeto** é MAPEADA de SNMP para WMI.        |
| [Macro de Convenção TEXTUAL](textual-convention-macro.md) | Como a macro de **Convenção textual** é MAPEADA de SNMP para WMI. |
| [Macro do tipo INTERCEPTAção](trap-type-macro.md)                   | Como a macro do **tipo Trap** é MAPEADA de SNMP para WMI.          |



 

O provedor SNMP vem com um compilador que converte objetos MIB em objetos WMI. O compilador SNMP também pode gerar um erro ou outras mensagens. Para obter mais informações, consulte [mensagens de erro do compilador SNMP](snmp-compiler-error-messages.md) e [mensagens de informações gerais](general-information-messages.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> </dl>

 

 



