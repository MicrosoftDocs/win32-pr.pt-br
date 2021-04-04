---
description: Fornece serviços para definir o código de CHV (verificação de titular de cartão) e para verificar o usuário.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interface ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662327"
---
# <a name="iscardverify-interface"></a>Interface ISCardVerify

\[A interface **ISCardVerify** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviço*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) . A interface **ISCardVerify** fornece serviços para configurar o código CHV (verificação de titular de cartão) e para verificar o usuário.

A classe **ISCardVerify** é definida para aplicativos que implementam a política CHV específica do aplicativo e que têm um conhecimento detalhado da implementação interna do cartão inteligente.

Veja a seguir um uso típico da interface **ISCardVerify** .

O procedimento a seguir usa **ISCardVerify** para alterar o código CHV.

**Para alterar o código CHV de um cartão inteligente**

1.  Crie uma interface **ISCardVerify** (por meio do método de interface [**ISCardManage**](iscardmanage.md) correspondente).
2.  Chame o método [**ChangeCode**](iscardverify-changecode.md) e forneça um novo código, especificando se ele é local ou global e se está habilitado ou desabilitado.
3.  Libere a interface **ISCardVerify** .

## <a name="members"></a>Membros

A interface **ISCardVerify** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardVerify** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardVerify** tem esses métodos.



| Método                                                        | Descrição                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Altera o código CHV atual.<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | Redefine o [*contexto de segurança*](../secgloss/s-gly.md) do cartão inteligente.<br/> |
| [**Bloqueá**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Habilita novamente o [*contexto de segurança*](../secgloss/s-gly.md).<br/>               |
| [**Verificar**](iscardverify-verify.md)                         | Autentica o usuário.<br/>                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



 

 
