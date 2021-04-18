---
title: Usando o controle ActiveX Área de Trabalho Remota
description: Como você pode usar o controle ActiveX Área de Trabalho Remota para personalizar a experiência do usuário do Serviços de Área de Trabalho Remota.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando o controle ActiveX do Área de Trabalho Remota
- Conexão Web de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando
- protocolo RDP Serviços de Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788026"
---
# <a name="using-the-remote-desktop-activex-control"></a>Usando o controle ActiveX Área de Trabalho Remota

Os tópicos a seguir contêm informações sobre como você pode usar o Área de Trabalho Remota controle ActiveX para personalizar a experiência do usuário do Serviços de Área de Trabalho Remota.

O controle ActiveX Área de Trabalho Remota está disponível nos seguintes formatos:

-   **O controle programável**— implementa interfaces que são seguras para scripts. Essa forma do controle pode ser usada por clientes da Web ou scripts (como VBScript) hosts.
-   **O controle não programável**— oferece funcionalidade adicional que não é segura para scripts. Essa forma do controle pode ser usada a partir de código nativo ou gerenciado, mas esse formulário não pode ser usado por clientes Web ou hosts somente de script.

A lista a seguir contém os s do **CLSID** para os diferentes controles para diferentes versões do sistema operacional. Cada um dos **CLSID** s é compatível com versões posteriores do sistema. Por exemplo, o **CLSID** para o controle programável no Windows Vista funcionará em versões posteriores do sistema, como o Windows 7.



| Versão do sistema                          | CLSID de controle programável             | CLSID de controle não programável          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1, Windows Server 2012 R2     | 301B94BA-5D25-4A12-BFFE-3B6E7A616585 | 8B918B82-7985-4C24-89DF-C33AD2BBFBCD |
| Windows 8, Windows Server 2012          | 5F681803-2900-4C43-A1CC-CF405404A676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7, Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54D38BF7-B1EF-4479-9674-1BD6EA465258 |
| Windows Vista com Service Pack 1 (SP1) | 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 | 4EB2F086-C818-447E-B32C-C51CE2B30D31 |



 

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Inserindo o controle ActiveX Área de Trabalho Remota em uma página da Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

Exemplo que demonstra o uso das interfaces programáveis.

</dd> <dt>

[Implementando canais virtuais programáveis usando o Conexão Web de Área de Trabalho Remota](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

Exemplos de código que mostram as etapas para implementar canais virtuais programáveis com Conexão Web de Área de Trabalho Remota.

</dd> <dt>

[Usando o controle ActiveX Área de Trabalho Remota com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar esse aplicativo para os computadores cliente.

</dd> <dt>

[Página da Web de exemplo incluída com o controle ActiveX Área de Trabalho Remota](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

Uma página da Web de exemplo (Default.htm) está no diretório onde Conexão Web de Área de Trabalho Remota está instalado.

</dd> <dt>

[Fornecendo para o RDP Client Security](providing-for-rdp-client-security.md)
</dt> <dd>

Algumas propriedades do objeto de controle ActiveX Área de Trabalho Remota são restritas a zonas de segurança de URL específicas do Internet Explorer.

</dd> <dt>

[Desabilitando recursos de Serviços de Área de Trabalho Remota](disabling-terminal-services-features.md)
</dt> <dd>

Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos.

</dd> </dl>

Para obter mais informações sobre a página da Web de exemplo incluída na instalação do controle ActiveX Área de Trabalho Remota, consulte a [página da Web de exemplo incluída com o controle activex área de trabalho remota](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 




