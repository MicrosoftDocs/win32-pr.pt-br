---
description: Um campo Database do tipo de dados FormattedSDDLText contém uma cadeia de caracteres de texto que descreve um descritor de segurança que usa SDDL (linguagem de definição de descritor de segurança) válida. Esse tipo de dados é usado pelo campo SDDLText da tabela MsiLockPermissionsEx para proteger um objeto selecionado. Observe que o campo SDDLText da tabela MsiLockPermissionsEx não oferece suporte a propriedades privadas ou públicas.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdfc4446c4362646e8c275ec427f759b8aec6a257d5221926431434688b91c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142885"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Um campo Database do tipo de dados **FormattedSDDLText** contém uma cadeia de caracteres de texto que descreve um descritor de segurança que usa SDDL ( [linguagem de definição de descritor de segurança](../secauthz/security-descriptor-definition-language.md) ) válida. Esse tipo de dados é usado pelo campo SDDLText da [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) para proteger um objeto selecionado. Observe que o campo SDDLText da tabela MsiLockPermissionsEx não oferece suporte a propriedades privadas ou públicas.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. esse tipo de dados está disponível a partir do Windows Installer 5,0.

O tipo de dados **FormattedSDDLText** pode conter uma cadeia de caracteres SDDL escrita em [formato de cadeia de caracteres de descritor de segurança](../secauthz/security-descriptor-string-format.md)válido. para obter mais informações sobre o SDDL, consulte a seção [controle de acesso](../secauthz/access-control.md) do [SDK (Software Development Kit) do Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/). Além disso, uma cadeia de texto **FormattedSDDLText** pode usar colchetes angulares (<>) para conter o domínio e o nome de usuário do usuário cujo Sid de conta deve ser determinado.

se o usuário que tem o nome de usuário *SampleUser* pertencer a um domínio chamado *SampleDomain*, o valor de **FormattedSDDLText** poderá identificar o proprietário usando a cadeia de caracteres de SID, o nome de usuário e o nome de domínio ou as variáveis de ambiente Windows. Por exemplo, as cadeias de caracteres a seguir seriam possíveis.

<dl> O:*proprietário \_ SID \_ String* G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; *\_ cadeia de \_ caracteres de SID do proprietário*) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD  
O: <*SampleDomain \\ SAMPLEUSER*>G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; <*SampleDomain \\ SampleUser*>) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD  
O: <\[ % UserDomain \] \\ \[ % username \]>G:Bad: (D; OICI; GA;;; BG) (A; OICI; GRGWGX;;; <\[ % UserDomain \] \\ \[ % username \]>) (A; OICI; GA;;; BA) S:ARAI (AU; SAFA; FA;;; WD
</dl>

 

 
