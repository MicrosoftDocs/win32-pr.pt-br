---
title: Discadores personalizados
description: Windows 2000 e sistemas operacionais posteriores permitem que os desenvolvedores forneçam seus próprios discadores personalizados que funcionam com o RAS (serviço de acesso remoto).
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

Windows 2000 e sistemas operacionais posteriores permitem que os desenvolvedores forneçam seus próprios discadores personalizados que funcionam com o RAS (serviço de acesso remoto). A discagem personalizada é implementada como uma única DLL (biblioteca de vínculo dinâmico) que exporta os seguintes pontos de entrada:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

A DLL de discagem personalizada deve exportar todos esses pontos de entrada e deve implementar os pontos de entrada como funções Unicode. para obter mais informações sobre essas funções, consulte a página de referência de cada função na referência do serviço de acesso remoto SDK do Windows.

Para que uma conexão RAS use a discagem personalizada, a entrada do catálogo telefônico para a conexão deve conter o caminho para a DLL de discagem personalizada. Use as funções de API RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para definir esse caminho no membro **szCustomDialDll** da estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para a entrada de catálogo telefônico.

## <a name="updating-the-registry-for-custom-dialers"></a>Atualizando o registro para discadores personalizados

Para que o sistema disque uma conexão que usa uma discagem personalizada, o caminho para a DLL de discagem personalizada deve existir no valor do registro a seguir.

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

Como **CustomDLL** é do tipo **reg \_ multi \_ sz**, ele pode conter caminhos para várias DLLs de discagem personalizada. Você precisa definir o caminho para a DLL de discagem personalizada nesse valor de registro, além da entrada de catálogo telefônico para a conexão.

Por padrão, esse valor de registro é gravável somente por um usuário com privilégios de administrador ou de sistema. Por motivos de segurança, não altere as permissões nessa chave do registro.

## <a name="using-custom-dialers-at-system-logon"></a>Usando discadores personalizados no logon do sistema

Windows 2000 e sistemas operacionais posteriores permitem que um usuário estabeleça uma conexão RAS no momento do logon. Para fazer isso, o usuário verifica o **logon usando a rede dial-up** na caixa de diálogo **informações de logon** . Depois que o usuário clicar no botão OK, o sistema exibirá as conexões disponíveis.

## <a name="security-considerations"></a>Considerações de segurança

Na maioria dos casos, uma discagem personalizada opera com os privilégios de segurança do usuário que a invoca. No entanto, se a discagem personalizada for invocada no logon, ela funcionará com privilégios de sistema. Portanto, projete a discagem personalizada para que ela não possa ser usada para violar a segurança do sistema. Por exemplo, a discagem não deve apresentar uma interface do usuário que permita ao usuário gravar o acesso ao sistema de arquivos do computador. as interfaces do usuário que fornecem esse acesso incluem a caixa de diálogo **Find-file** , a caixa de diálogo comum **abrir arquivo** e Windows **ajuda**.

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>A interface do usuário do discador personalizado deve dar suporte a IDCANCEL

Se a discagem personalizada exibir uma interface do usuário, a interface do usuário deverá dar suporte a \_ mensagens de comando do WM em que LOWORD (*wParam*) seja igual a IDCANCEL.

 

 