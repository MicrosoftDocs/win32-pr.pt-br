---
title: Discadores personalizados
description: Windows sistemas operacionais 2000 e posteriores permitem que os desenvolvedores forneçam seus próprios discadores personalizados que funcionam com o RAS (Serviço de Acesso Remoto).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Discadores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791496"
---
# <a name="custom-dialers"></a>Discadores personalizados

Windows sistemas operacionais 2000 e posteriores permitem que os desenvolvedores forneçam seus próprios discadores personalizados que funcionam com o RAS (Serviço de Acesso Remoto). O discador personalizado é implementado como uma única DLL (biblioteca de vínculo dinâmico) que exporta os seguintes pontos de entrada:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustom Ltda**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

A DLL de discagem personalizada deve exportar todos esses pontos de entrada e deve implementar os pontos de entrada como funções Unicode. Para obter mais informações sobre essas funções, consulte a página de referência para cada função na Referência do Serviço de Acesso Remoto Windows SDK.

Para que uma conexão RAS use o discador personalizado, a entrada de phone-book para a conexão deve conter o caminho para a DLL de discagem personalizada. Use as funções de API ras [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir esse caminho no **membro szCustomDialDll** da estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para a entrada de phone-book.

## <a name="updating-the-registry-for-custom-dialers"></a>Atualizando o Registro para Discadores Personalizados

Para que o sistema disce uma conexão que usa um discador personalizado, o caminho para a DLL de discagem personalizada deve existir no valor do Registro a seguir.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Como **CustomDLL** é do tipo **REG MULTI \_ \_ SZ**, ela pode conter caminhos para várias DLLs de discagem personalizadas. Você precisa definir o caminho para a DLL de discagem personalizada nesse valor do Registro, além da entrada de phone-book para a conexão.

Por padrão, esse valor do Registro só pode ser escrito por um usuário com privilégios de Administrador ou Sistema. Por motivos de segurança, não altere as permissões nesta chave do Registro.

## <a name="using-custom-dialers-at-system-logon"></a>Usando discadores personalizados no logon do sistema

Windows sistemas operacionais 2000 e posteriores permitem que um usuário estabeleça uma conexão RAS no momento do logon. Para fazer isso, o usuário verifica **Logon usando a** Rede Discar na caixa **de diálogo Informações de** Logon. Depois que o usuário clica no botão Ok, o sistema exibe as conexões disponíveis.

## <a name="security-considerations"></a>Considerações de segurança

Na maioria dos casos, um discador personalizado opera com os privilégios de segurança do usuário que o invoca. No entanto, se o discador personalizado for invocado no logon, ele operará com privilégios do sistema. Portanto, projete o discador personalizado para que ele não possa ser usado para violar a segurança do sistema. Por exemplo, o discador não deve apresentar uma interface do usuário que permita ao usuário gravar o acesso ao sistema de arquivos do computador. As interfaces do usuário que fornecem esse  acesso incluem a caixa de diálogo **Find-File,** a caixa de diálogo comum Abrir Arquivo e Windows **Ajuda**.

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>Os Interface do Usuário de discagem personalizada devem dar suporte a IDCANCEL

Se o discador personalizado exibir uma interface do usuário, a interface do usuário deverá dar suporte a mensagens WM COMMAND em que \_ LOWORD(*wParam*) é igual a IDCANCEL.

 

 