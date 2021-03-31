---
description: A ferramenta SetReg define o valor das chaves do registro que controlam o comportamento do processo de verificação do certificado Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05da29d3eddf7e04ba5bd735e1032f388d9d204a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646666"
---
# <a name="setreg"></a>SetReg

A ferramenta SetReg define o valor das chaves do registro que controlam o comportamento do processo de verificação do certificado Authenticode. Essas chaves são chamadas de chaves de estado de publicação de software. Depois de concluir a ação solicitada, a ferramenta exibe o estado atual das chaves de estado de publicação de software.

**Setreg** \[ *Opções* \] do \[ *Opção \#* {**true** \| **false**}\]

A ferramenta Set Registry só é fornecida com o .NET Framework SDK versão 1,0 e 1,1, que você pode baixar do [centro de download da Microsoft](https://www.microsoft.com/download/details.aspx?id=16217).

## <a name="options"></a>Opções

As opções podem ser um dos valores a seguir. As opções fornecidas na tabela a seguir podem ser usadas somente com o Internet Explorer 4,0 ou posterior.



| Opção | Descrição                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Suprimir a exibição dos valores de chave de estado de publicação de software depois de SetReg concluir a ação solicitada. Os valores são exibidos por padrão. |
| **-?** | Listar a sintaxe e as opções de comando.                                                                                                                       |



 

## <a name="choice-"></a>Desejada \#

*Opção \#* deve ser um dos valores a seguir.



| Escolha | Descrição                                                                                                                       | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Confiar na raiz do teste                                                                                                               | Esse valor é ignorado. **Windows XP/2000:** Se **for true**, confiará em uma raiz de teste. Isso é equivalente a executar "regedit wvtston. reg" no Internet Explorer 3. *x*.<br/> O padrão é **false**. Qualquer arquivo assinado com uma raiz de teste não será verificado, a menos que esse sinalizador seja definido como **true**. Observe que esse comportamento foi alterado com o Windows XP com Service Pack 1 (SP1) porque o Windows XP com SP1 ignora esse valor.<br/> <br/> |
| **2**  | Usar data de validade em certificados                                                                                               | Se **for true**, verificará a data de expiração do certificado. Para ignorar as datas de expiração, defina esse sinalizador como **false**. O padrão é **true**.                                                                                                                                                                                                                                                                                                       |
| **3**  | Verificar a [ *lista de revogação*](../secgloss/c-gly.md) | Se **for true**, executará a verificação de revogação. Para ignorar a verificação de revogação, defina esse sinalizador como **false**. O padrão é **true**. **Internet Explorer 3. *x*:** o padrão é **false**.<br/>                                                                                                                                                                                                                                               |
| **4**  | Servidor de revogação offline OK (individual)<br/>                                                                              | Se **for true**, permitirá a aprovação offline para certificados individuais. O padrão é **false**.                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Servidor de revogação offline OK (comercial)<br/>                                                                              | Se **for true**, permitirá a aprovação offline para certificados comerciais. O padrão é **true**.                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Servidor de revogação offline Java OK (individual)<br/>                                                                         | Se **for true**, permitirá a aprovação offline para certificados individuais e não exibirá a interface do usuário para certificados inválidos. O padrão é **false**.                                                                                                                                                                                                                                                                                    |
| **7**  | Servidor de revogação offline Java OK (comercial)<br/>                                                                         | Se **for true**, permitirá a aprovação offline para certificados comerciais e não exibirá a interface do usuário para certificados inválidos. O padrão é **true**.                                                                                                                                                                                                                                                                                     |
| **8**  | Tornar os objetos assinados da versão 1 não mais válidos                                                                                     | Se **for true**, tornará os objetos assinados da versão 1 que não são mais válidos. O padrão é **false**.                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Verificar a lista de revogação do servidor de carimbo de data/hora                                                                                | Se **for true**, executará a verificação de revogação no certificado do servidor de carimbo de data/hora. O padrão é **false**. **Internet Explorer 3. *x*:** não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                            |
| **10** | Somente itens de confiança encontrados no banco de dados de confiança                                                                                      | Se **verdadeiro**, permite downloads de Publicadores que estão contidos no banco de dados de confiança pessoal. O padrão é **false**. **Internet Explorer 3. *x*:** não há suporte para esse valor.<br/>                                                                                                                                                                                                                                             |



 

 

 
