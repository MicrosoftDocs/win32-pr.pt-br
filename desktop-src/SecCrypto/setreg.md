---
description: A ferramenta SetReg define o valor das chaves do Registro que controlam o comportamento do processo de verificação de certificado Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267aa140cad713e550ddf8afd0281d489bdd90ac0b26a7f7a4781240ecac24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900296"
---
# <a name="setreg"></a>SetReg

A ferramenta SetReg define o valor das chaves do Registro que controlam o comportamento do processo de verificação de certificado Authenticode. Essas chaves são chamadas de Chaves de Estado de Publicação de Software. Depois de concluir a ação solicitada, a ferramenta exibe o estado atual das Chaves de Estado de Publicação de Software.

**SetReg** \[ *Opções* \] \[ *Escolha \#* {**TRUE** \| **FALSE**}\]

A ferramenta Definir Registro é fornecidas apenas com o SDK do .NET Framework versão 1.0 e .1.1, que você pode baixar no Centro de Download da [Microsoft.](https://www.microsoft.com/download/details.aspx?id=16217)

## <a name="options"></a>Opções

As opções podem ser um dos valores a seguir. As opções fornecidas na tabela a seguir podem ser usadas somente com Internet Explorer 4.0 ou posterior.



| Opção | Descrição                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Suprimir a exibição dos valores de Chave de Estado de Publicação de Software depois que SetReg concluir a ação solicitada. Os valores são exibidos por padrão. |
| **-?** | Listar a sintaxe e as opções do comando.                                                                                                                       |



 

## <a name="choice-"></a>Escolha \#

*Escolha \#* deve ser um dos valores a seguir.



| Escolha | Descrição                                                                                                                       | Resultado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Confiar na raiz do teste                                                                                                               | Esse valor é ignorado. **Windows XP/2000:** Se **TRUE**, confiará em uma raiz de teste. Isso é equivalente à execução de "regedit wvtavo.reg" Internet Explorer 3. *x*.<br/> O padrão é **FALSE.** Qualquer arquivo assinado com uma raiz de teste não verificará, a menos que esse sinalizador esteja definido como **TRUE.** Observe que esse comportamento foi alterado com Windows XP com Service Pack 1 (SP1) porque Windows XP com SP1 ignora esse valor.<br/> <br/> |
| **2**  | Usar a data de validade em certificados                                                                                               | Se **TRUE**, verifica a data de validade do certificado. Para ignorar datas de expiração, de definir esse sinalizador como **FALSE.** O padrão é **TRUE.**                                                                                                                                                                                                                                                                                                       |
| **3**  | Verificar a [ *lista de revogação*](../secgloss/c-gly.md) | Se **TRUE**, executará a verificação de revogação. Para ignorar a verificação de revogação, de definir esse sinalizador como **FALSE.** O padrão é **TRUE.** **Internet Explorer 3. *x:*** o padrão é **FALSE.**<br/>                                                                                                                                                                                                                                               |
| **4**  | Servidor de revogação offline OK (individual)<br/>                                                                              | Se **TRUE**, permitirá a aprovação offline para certificados individuais. O padrão é **FALSE.**                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Servidor de revogação offline OK (Comercial)<br/>                                                                              | Se **TRUE**, permitirá a aprovação offline para certificados comerciais. O padrão é **TRUE.**                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Java offline Revocation server OK (Individual)<br/>                                                                         | Se **TRUE**, permitirá a aprovação offline para certificados individuais e não exibirá a interface do usuário para certificados ruins. O padrão é **FALSE.**                                                                                                                                                                                                                                                                                    |
| **7**  | Servidor de revogação offline do Java OK (Comercial)<br/>                                                                         | Se **TRUE**, permitirá a aprovação offline para certificados comerciais e não exibirá a interface do usuário para certificados ruins. O padrão é **TRUE.**                                                                                                                                                                                                                                                                                     |
| **8**  | Tornar objetos assinados da versão 1 não são mais válidos                                                                                     | Se **TRUE**, torna os objetos assinados da versão 1 não mais válidos. O padrão é **FALSE.**                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Verificar a lista de revogação do servidor de carimbo de data/hora                                                                                | Se **TRUE**, executará a verificação de revogação no certificado do servidor de carimbo de data/hora. O padrão é **FALSE.** **Internet Explorer 3. *x:*** não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                            |
| **10** | Somente itens de confiança encontrados no banco de dados de confiança                                                                                      | Se **TRUE**, permitirá downloads de editores contidos no Banco de Dados de Confiança Pessoal. O padrão é **FALSE.** **Internet Explorer 3. *x:*** não há suporte para esse valor.<br/>                                                                                                                                                                                                                                             |



 

 

 
