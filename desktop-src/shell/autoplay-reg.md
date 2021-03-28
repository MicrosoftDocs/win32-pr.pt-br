---
description: Há muitas situações em que a execução automática pode precisar ser temporariamente desabilitada ou persistente.
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: Habilitando e desabilitando o AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370618"
---
# <a name="enabling-and-disabling-autorun"></a>Habilitando e desabilitando o AutoRun

Há muitas situações em que a execução automática pode precisar ser temporariamente desabilitada ou persistente. Por exemplo, o AutoRun pode interferir na operação de um aplicativo em execução e precisa ser desabilitado durante a duração. O sistema fornece várias maneiras de desabilitar o AutoRun.

-   [Suprimindo o AutoRun programaticamente](#suppressing-autorun-programmatically)
-   [Usando o registro para desabilitar o AutoRun](#using-the-registry-to-disable-autorun)
-   [AutoRun para outros tipos de mídia de armazenamento](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>Suprimindo o AutoRun programaticamente

Há uma variedade de situações em que a execução de AutoRun pode precisar ser suprimida programaticamente. Dois exemplos são:

-   Seu aplicativo tem um programa de instalação que exige que o usuário insira outro disco que possa conter um arquivo autorun. inf.
-   Durante a operação do seu aplicativo, o usuário pode precisar inserir outro disco que possa conter um arquivo autorun. inf.

Em ambos os casos, normalmente você não vai querer iniciar outro aplicativo enquanto o original está em andamento.

Os usuários podem suprimir manualmente o AutoRun mantendo a tecla SHIFT pressionada ao inserir o CD-ROM. No entanto, geralmente é preferível lidar com essa operação programaticamente, em vez de depender do usuário.

Com sistemas que têm o Shell [versão 4,70](versions.md) e posterior, o Windows envia uma mensagem "QueryCancelAutoPlay" para a janela em primeiro plano. Seu aplicativo pode responder a esta mensagem para suprimir o AutoRun. Essa abordagem é usada por utilitários do sistema, como a caixa de diálogo [abrir](../dlgbox/open-and-save-as-dialog-boxes.md) comum para desabilitar o autorun.

Os fragmentos de código a seguir ilustram como configurar e tratar essa mensagem. Seu aplicativo deve estar em execução na janela em primeiro plano. Primeiro, registre "QueryCancelAutoPlay" como uma mensagem do Windows:


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



A janela do seu aplicativo deve estar no primeiro plano para receber esta mensagem. O manipulador de mensagens deve retornar **true** para cancelar autorun e **false** para habilitá-lo. O fragmento de código a seguir ilustra como usar essa mensagem para desabilitar o AutoRun.


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



Se seu aplicativo estiver usando uma caixa de diálogo e precisar responder a uma mensagem "QueryCancelAutoPlay", ele não poderá simplesmente retornar **true** ou **false**. Em vez disso, chame [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) com *NIndex* definido como **DWL \_ MSGRESULT**. Defina o parâmetro *dwNewLong* como **true** para cancelar o autorun e **false** para habilitá-lo. Por exemplo, o procedimento de caixa de diálogo de exemplo a seguir cancela o AutoRun quando recebe uma mensagem "QueryCancelAutoPlay".


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a>Usando o registro para desabilitar o AutoRun

Há dois valores de registro que podem ser usados para desabilitar o AutoRun de forma persistente: NoDriveAutoRun e NoDriveTypeAutoRun. O primeiro valor desabilita o AutoRun para as letras de unidade especificadas e a segunda desabilita o AutoRun para uma classe de unidades. Se um desses valores for definido para desabilitar o AutoRun para um dispositivo específico, ele será desabilitado. Consulte o artigo da base de dados de conhecimento [como desabilitar a funcionalidade de Autorun no Windows](https://support.microsoft.com/kb/967715) para obter mais informações sobre como desabilitar a funcionalidade de Autorun. Este artigo lista as diferentes atualizações que você deve ter instaladas para desabilitar corretamente a funcionalidade de Autorun.

> [!Note]  
> Os valores NoDriveAutoRun e NoDriveTypeAutoRun só devem ser modificados pelos administradores do sistema para alterar o valor de todo o sistema para fins de teste ou administrativos. Os aplicativos não devem modificar esses valores, pois não há como restaurá-los de forma confiável para seus valores originais.

 

O valor NoDriveAutoRun desabilita o AutoRun para as letras de unidade especificadas. É um valor de \_ dados reg DWORD, encontrado na seguinte chave:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

O primeiro bit do valor corresponde à unidade A:, a segunda a B: e assim por diante. Para desabilitar o AutoRun para uma ou mais letras de unidade, defina os bits correspondentes. Por exemplo, para desabilitar as unidades a: e C:, defina NoDriveAutoRun como `0x00000005` .

O valor de NoDriveTypeAutoRun desabilita a execução automática para uma classe de unidades. É um valor de \_ dados binário reg de 4 bytes ou reg DWORD \_ , encontrado na mesma chave.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

Ao definir os bits do primeiro byte deste valor, unidades diferentes podem ser excluídas do trabalho com AutoRun.

A tabela a seguir fornece as constantes bits e bitmask, que podem ser definidas no primeiro byte de NoDriveTypeAutoRun para desabilitar o AutoRun para um determinado tipo de unidade. Você deve reiniciar o Windows Explorer antes que as alterações entrem em vigor.



| Número de bits | Constante de bitmask      | Description                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **UNIDADE \_ REmovida** | O disco pode ser removido da unidade (como um disquete). |
| 0x08       | **UNIDADE \_ fixa**      | O disco não pode ser removido da unidade (um disco rígido).        |
| 0x10       | **UNIDADE \_ remota**     | Unidade de rede.                                          |
| 0x20       | **UNIDADE de \_ cdrom**      | Unidade de CD-ROM.                                           |
| 0x40       | **UNIDADE de \_ ramdisk**    | Disco RAM.                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>AutoRun para outros tipos de mídia de armazenamento

A execução automática destina-se principalmente à distribuição pública de aplicativos em CD-ROM e DVD-ROM, e seu uso não é recomendado para outras mídias de armazenamento. No entanto, geralmente é útil habilitar o AutoRun em outros tipos de mídia de armazenamento removível. Normalmente, esse recurso é usado para simplificar a depuração de arquivos AutoRun. inf. O AutoRun só funciona em dispositivos de armazenamento removíveis quando os critérios a seguir são atendidos:

-   O dispositivo deve ter drivers compatíveis com AutoRun. Para ser compatível com AutoRun, um driver deve notificar o sistema de que um disco foi inserido enviando uma mensagem do [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .
-   O diretório raiz da mídia inserida deve conter um arquivo autorun. inf.
-   O dispositivo não deve ter o AutoRun desabilitado por meio do [registro](#using-the-registry-to-disable-autorun).
-   O aplicativo em primeiro plano não [eliminou](#suppressing-autorun-programmatically) o autorun.

> [!Note]  
> Esse recurso não deve ser usado para distribuir aplicativos em mídias removíveis. Como a implementação do AutoRun em mídia removível fornece uma maneira fácil de espalhar vírus de computador, os usuários devem ser suspeitos de qualquer disquete distribuído publicamente que contenha um arquivo autorun. inf.

 

Normalmente, o AutoRun é iniciado automaticamente, mas também pode ser iniciado manualmente. Se o dispositivo atender aos critérios listados acima, o menu de atalho da letra da unidade incluirá um comando de **reprodução automática** . Para executar o AutoRun manualmente, clique com o botão direito do mouse no ícone da unidade e selecione **reprodução automática** no menu de atalho ou clique duas vezes no ícone da unidade. Se os drivers não forem compatíveis com AutoRun, o menu de atalho não terá um item de **reprodução automática** e o autorun não poderá ser iniciado.

Os drivers compatíveis com AutoRun são fornecidos com algumas unidades de disco removíveis, bem como alguns outros tipos de mídia removível, como placas CompactFlash. O AutoRun também funciona com unidades de rede que são mapeadas para uma letra de unidade com o Windows Explorer ou montados com o [MMC (console de gerenciamento Microsoft)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page). Assim como ocorre com o hardware montado, uma unidade de rede montada deve ter um arquivo autorun. inf em seu diretório raiz e não deve ser desabilitada por meio do [registro](#using-the-registry-to-disable-autorun).

 

 
