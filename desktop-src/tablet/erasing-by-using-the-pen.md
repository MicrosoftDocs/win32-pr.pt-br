---
description: Se você optar por implementar o apagamento em seu aplicativo que não seja usando o objeto InkOverlay, poderá fazer isso usando um dos dois métodos a seguir.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Apagando usando a caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370651"
---
# <a name="erasing-by-using-the-pen"></a>Apagando usando a caneta

Se você optar por implementar o apagamento em seu aplicativo que não seja usando o objeto [**InkOverlay**](inkoverlay-class.md) , poderá fazer isso usando um dos dois métodos a seguir.

## <a name="using-the-tip-of-the-pen"></a>Usando a ponta da caneta

A ponta da caneta eletrônica geralmente é usada para manuscrito e desenho; no entanto, a dica também pode ser usada para apagar a tinta. Para fazer isso, o aplicativo deve ter um modo de apagamento que os usuários podem empregar. Nesse modo, use o teste de clique para determinar a tinta que o cursor está movendo. Você pode definir o modo de apagamento para excluir apenas a tinta que o cursor passa ou traços inteiros que interseccionam o caminho do cursor, dependendo do design ou das considerações funcionais.

Para obter um exemplo de como usar um modo de apagamento para apagar a tinta, consulte o [exemplo de apagamento de tinta](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Usando a parte superior da caneta

Para implementar o apagamento com a parte superior da caneta do Tablet, seu aplicativo deve procurar uma alteração no cursor. Para procurar o cursor invertido, ouça o evento [**CursorInRange**](inkoverlay-cursorinrange.md) para determinar quando o cursor está dentro do contexto do seu aplicativo. Quando o cursor estiver no intervalo, procure a propriedade [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) no objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) . Se a propriedade **invertida** for **true**, execute o teste de clique para determinar a tinta que o cursor está movendo. Apague a tinta ou os traços que interseccionam o caminho do cursor, dependendo do design ou das considerações funcionais.

Para obter um exemplo de como usar a parte superior da caneta para apagar a tinta, consulte o [exemplo de apagamento de tinta](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Determinando se o apagamento com a parte superior da caneta está habilitado

Os usuários podem usar o topo da caneta para apagar a tinta em aplicativos criados para Tablet PC, se o hardware específico permitir. Essa funcionalidade é acessada por uma caixa de seleção na caixa de grupo botões de caneta na guia Opções de caneta do diálogo painel de controle configurações de Tablet e caneta. Para detectar se o usuário ativou o apagamento para a parte superior da caneta, verifique a seguinte subchave do registro:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

A `EraseEnable` entrada dessa subchave é do tipo **reg \_ DWORD**. O valor dessa entrada é 1 para habilitado, ou 0 para desabilitado. Outros valores são reservados para uso futuro.

Se seu aplicativo permitir que a parte superior da caneta seja usada para apagar, você deverá verificar e armazenar em cache o valor da entrada EraseEnable quando:

-   O aplicativo é iniciado.
-   Sempre que seu aplicativo receber o foco depois de perder o foco.

Use esse valor em cache para modificar o comportamento do seu aplicativo adequadamente.

O exemplo C a seguir \# define um `GetEraseEnabled` método que verifica o valor da `EraseEnable` entrada da `SysEventParameters` subchave. O `GetEraseEnabled` método retornará **true** se o valor da entrada for 1; retornará **false** se o valor da entrada for 0; ou lançar uma exceção [InvalidOperationException](/dotnet/api/system.invalidoperationexception) se o valor da entrada for diferente de 1 ou 0. O `GetEraseEnabled` método retornará o valor esperado **true** se a subchave ou a entrada não estiver presente.


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
