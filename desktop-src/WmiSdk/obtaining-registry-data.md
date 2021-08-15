---
description: Você pode obter ou modificar dados do Registro usando a classe StdRegProv da WMI e seus métodos.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Obtendo dados do Registro
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b904316809a6949c6897e32127f85569e3b2ac13cb769db4739e61c164aa19fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050634"
---
# <a name="obtaining-registry-data"></a>Obtendo dados do Registro

Você pode obter ou modificar dados do Registro usando a classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) da WMI e seus métodos. Embora use o utilitário Regedit para exibir e alterar valores do Registro no computador local, **StdRegProv** permite que você use um script ou aplicativo para automatizar essas atividades no computador local e computadores remotos.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contém métodos para fazer o seguinte:

-   Verificar as permissões de acesso para um usuário
-   Criar, enumerar e excluir chaves do Registro
-   Criar, enumerar e excluir subkeys ou valores nomeados
-   Ler, gravar e excluir valores de dados

Os dados do Registro são organizados por subárvores, chaves e sub-chaves aninhadas em uma chave de nível superior. Os valores de dados reais são chamados de entradas ou valores nomeados.

As subárvores incluem o seguinte:

-   **HKEY \_ CLASSES \_ ROOT** (abreviado como **HKCR**)
-   **HKEY \_ USUÁRIO \_ ATUAL** (**HKCU**)
-   **HKEY \_ COMPUTADOR \_ LOCAL** (**HKLM**)
-   **USUÁRIOS \_ DO HKEY**
-   **CONFIGURAÇÃO \_ ATUAL DO HKEY \_**

Por exemplo, na entrada do Registro **HKEY** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**,  a subárvore HKEY é SOFTWARE ; as sub-chaves são Microsoft e DirectX ; e a entrada de valor nomeado é **InstalledVersion**.

Um [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ocorre quando ocorre uma alteração em uma chave específica, mas a entrada não identifica como os valores são alterados nem esse evento será disparado por alterações abaixo da chave especificada. Para identificar alterações em qualquer lugar em uma estrutura de chave hierárquica, use [**o RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), que não retorna valores específicos ou alterações de chave que ocorrem. Para obter uma alteração de valor de entrada específica, use [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)e, em seguida, leia a entrada para obter um valor de linha de base.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) tem apenas métodos que podem ser chamados de C++ ou script, que é diferente da estrutura de classe Win32.

O exemplo de código a seguir mostra como usar o [**método StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) para listar todas as sub-chaves de software da Microsoft na chave do Registro.

**HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** \\  \\ **Microsoft**


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





[**StdRegProv tem**](/previous-versions/windows/desktop/regprov/stdregprov) métodos diferentes para ler os vários tipos de dados de valor de entrada do Registro. Se a entrada tiver valores desconhecidos, você poderá chamar [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para listá-los. A tabela a seguir lista a correspondência entre **os métodos StdRegProv** e os tipos de dados.



| Método                                                                                  | Tipo de Dados           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

A tabela a seguir lista os métodos correspondentes para criar novas chaves ou valores ou alterar os existentes.



| Método                                                                                  | Tipo de Dados           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

O exemplo a seguir mostra como ler a lista de fontes para o log de eventos do sistema da chave do Registro.

**HKEY \_ Sistema \_ DE COMPUTADOR LOCAL** Sistema Atual Conjunto de \\  \\  \\ **Controles** \\ **Sistema De Eventos** Sistema De Eventos \\ **Sistema**

Observe que os itens no valor de multistring são tratados como uma coleção ou matriz.


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



O provedor do Registro é hospedado em LocalService, não no LocalSystem. Portanto, não é possível obter informações remotamente da subárvore **HKEY \_ CURRENT \_ USER.** No entanto, os scripts executados no computador local ainda podem acessar **o USUÁRIO \_ ATUAL \_ do HKEY.** Você pode definir o modelo de hospedagem como LocalSystem em um computador remoto, mas esse é um risco de segurança porque o registro no computador remoto está vulnerável a acesso inaceitável. Para obter mais informações, consulte [Hospedagem e segurança do provedor.](provider-hosting-and-security.md)

## <a name="examples"></a>Exemplos

O [exemplo de código](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) Ler um valor de Registro Binário VBScript na Galeria do TechNet usa o WMI para ler um valor de registro binário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas WMI: Registro](wmi-tasks--registry.md)
</dt> </dl>

 

 
