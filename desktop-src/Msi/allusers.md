---
Description: A propriedade ALLUSERS configura o contexto de instalação do pacote.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Propriedade ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: b6412707d6ef46b55d1f8add3de56a24e6f970dc9fa7f0353dce6ec9efa9f531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581876"
---
# <a name="allusers-property"></a>Propriedade ALLUSERS

A propriedade **AllUsers** configura o contexto de instalação do pacote. o Windows Installer executa uma instalação por usuário ou instalação por máquina, dependendo dos privilégios de acesso do usuário, se forem necessários privilégios elevados para instalar o aplicativo, o valor da propriedade **ALLUSERS** , o valor da propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) e a versão do sistema operacional.

O valor da propriedade **AllUsers** , no momento da instalação, determina o [contexto de instalação](installation-context.md).

-   Um valor de propriedade **AllUsers** de 1 especifica o contexto de instalação por máquina.
-   Um valor de propriedade **AllUsers** de uma cadeia de caracteres vazia ("") especifica o contexto de instalação por usuário.
-   se o valor da propriedade **allusers** for definido como 2, o Windows Installer sempre redefinirá o valor da propriedade **allusers** como 1 e executará uma instalação por computador ou redefinirá o valor da propriedade **allusers** como uma cadeia de caracteres vazia ("") e executará uma instalação por usuário. O valor ALLUSERS = 2 permite que o sistema redefina o valor de **AllUsers** e o contexto de instalação, dependendo dos privilégios do usuário e da versão do Windows.

    **Windows 7:** Defina a propriedade **AllUsers** como 2 para usar a propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) para especificar o contexto de instalação. Defina a propriedade **MSIINSTALLPERUSER** como uma cadeia de caracteres vazia ("") para uma instalação por máquina. Defina a propriedade **MSIINSTALLPERUSER** como 1 para uma instalação por usuário. Se o pacote tiver sido escrito seguindo as diretrizes de desenvolvimento descritas em [criação de pacote único](single-package-authoring.md), os usuários que tiverem acesso de usuário poderão instalar no contexto por usuário sem precisar fornecer credenciais do UAC. Se o usuário tiver privilégios de acesso de usuário, o instalador executará uma instalação por máquina somente se as credenciais de administrador forem fornecidas para a caixa de diálogo do UAC.

    **Windows Vista:** defina a propriedade **ALLUSERS** como 2 e Windows Installer está em conformidade com o UAC ( [*controle de conta de usuário*](u-gly.md) ). Se o usuário tiver privilégios de acesso de usuário e ALLUSERS = 2, o instalador executará uma instalação por máquina somente se as credenciais de administrador forem fornecidas para a caixa de diálogo do UAC. Se o UAC estiver habilitado e as credenciais de administrador corretas não forem fornecidas, a instalação falhará com um erro informando que privilégios de administrador são necessários. Se o UAC for desabilitado pela chave do registro, pela política de grupo ou pelo painel de controle, a caixa de diálogo UAC não será exibida e a instalação falhará com um erro informando que privilégios de administrador são necessários.

    **Windows XP:** defina a propriedade **ALLUSERS** como 2 e Windows Installer executará uma instalação por usuário se o usuário tiver privilégios de acesso de usuário.

-   se o valor da propriedade **ALLUSERS** não for igual a 2, o Windows Installer ignorará o valor da propriedade [**MSIINSTALLPERUSER**](msiinstallperuser.md) .

## <a name="example"></a>Exemplo

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

exemplo de [exemplos clássicos Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) em GitHub.

## <a name="default-value"></a>Valor padrão

O contexto de instalação padrão recomendado é por usuário. Se **AllUsers** não estiver definido, o instalador fará uma instalação por usuário. Você pode garantir que a propriedade **AllUsers** não tenha sido definida definindo seu valor como uma cadeia de caracteres vazia (""), ALLUSERS = "".

## <a name="remarks"></a>Comentários

O [contexto de instalação](installation-context.md) determina os valores das propriedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) . O contexto de instalação determina as partes do registro em que as entradas na [tabela de registro](registry-table.md) e na [tabela RemoveRegistry](removeregistry-table.md), com-1 na coluna raiz, são gravadas ou removidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[Contexto de instalação](installation-context.md)
</dt> <dt>

[Criação de pacote único](single-package-authoring.md)
</dt> </dl>

 

 




