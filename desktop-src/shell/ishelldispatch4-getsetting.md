---
description: Método IShellDispatch4. Configuration – recupera uma configuração de shell global.
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: Método IShellDispatch4. GetSetting (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ec31516f88dc9b79169a0272cfca735080e28aaebc81ac49cc7a8b083bc9377e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720850"
---
# <a name="ishelldispatch4getsetting-method"></a>Método IShellDispatch4. GetSetting

Recupera uma configuração de shell global.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lSetting* \[ no\]
</dt> <dd>

Tipo: **longo**

Um valor que especifica a configuração de shell atual a ser recuperada. Apenas uma configuração pode ser recuperada em cada chamada. Os valores a seguir são reconhecidos por este método.

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)


</dt> <dd>

**Windows Vista e posterior**. O estado da opção **usar caixas de seleção para selecionar itens** . Essa opção é habilitada automaticamente quando o sistema tem um dispositivo de entrada de caneta configurado.

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)


</dt> <dd>

Não usado.

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)


</dt> <dd>

O estado da opção **permitir todos os nomes em maiúsculas** . a partir do Windows Vista, essa opção de pasta não está mais disponível.

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)


</dt> <dd>

O estado do **clique duplo para abrir uma opção de item (clique único para selecionar)** .

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)


</dt> <dd>

Não usado.

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)


</dt> <dd>

Não usado.

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)


</dt> <dd>

o estado do ícone de exibição na exibição de lista do Windows Explorer. Se essa opção estiver ativa, nenhum ícone será exibido na exibição de lista.

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)


</dt> <dd>

**Windows Vista e posterior**. o estado do nome de exibição é exibido na exibição de lista do Windows Explorer. Se essa opção estiver ativa, os ícones serão exibidos no modo de exibição de lista, mas os nomes de exibição não serão.

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)


</dt> <dd>

O estado do **botão Mostrar unidade de rede do mapa na opção da barra de ferramentas** . a partir do Windows Vista, essa opção não está mais disponível.

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)


</dt> <dd>

O estado da opção da caixa de **diálogo de confirmação de exclusão de exibição** da lixeira.

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)


</dt> <dd>

O estado da opção **Pesquisar automaticamente pastas e impressoras de rede** . a partir do Windows Vista, essa opção não está mais disponível.

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)


</dt> <dd>

O estado das **janelas de pasta de inicialização em uma opção de processo separada** .

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)


</dt> <dd>

Não usado.

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)


</dt> <dd>

O estado da opção **arquivos e pastas ocultos** .

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)


</dt> <dd>

O estado da opção **Mostrar atributos de arquivo no modo de exibição de detalhes** . a partir do Windows Vista, essa opção não está mais disponível.

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)


</dt> <dd>

O estado da opção **Mostrar arquivos NTFS criptografados ou compactados na cor** .

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ Conextensões** (0x00000002)


</dt> <dd>

O estado da opção **Ocultar extensões para tipos de arquivo conhecidos** .

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)


</dt> <dd>

O estado da opção **mostrar descrição pop-up para itens da pasta e da área de trabalho** .

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ 0x00400000 (nastartpage** )


</dt> <dd>

Não usado.

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)


</dt> <dd>

O estado da opção **ocultar arquivos protegidos do sistema operacional** .

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)


</dt> <dd>

O estado da opção **arquivos e pastas ocultos** . no Windows Vista e posterior, isso é equivalente a SSF \_ SHOWALLOBJECTS. em versões do Windows antes Windows Vista, esse valor se refere ao estado da opção **não mostrar arquivos e pastas ocultos** .

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)


</dt> <dd>

**Windows Vista e posterior**. O estado do **ícone do arquivo de exibição na opção de miniaturas** . Se essa opção estiver ativa, uma sobreposição de tipo de arquivo será aplicada quando um arquivo fornecer uma representação em miniatura.

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)


</dt> <dd>

Não usado.

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)


</dt> <dd>

o estado da opção de exibição Windows xp, que seleciona entre o estilo Windows XP e o estilo clássico. a partir do Windows Vista, essa opção não está mais disponível.

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)


</dt> <dd>

O estado da **exibição como uma opção de exibição da Web**. a partir do Windows Vista, essa opção não está mais disponível.

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)


</dt> <dd>

O estado da opção de **estilo clássico** . a partir do Windows Vista, essa opção não está mais disponível.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **\_ booliano \* de variante**

Definir como **true** se a configuração existir; caso contrário, **false**.

### <a name="vb"></a>VB

Tipo: **\_ booliano \* de variante**

Definir como **true** se a configuração existir; caso contrário, **false**.

## <a name="examples"></a>Exemplos

os exemplos a seguir mostram o uso de **getdefinition** para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 6,0 ou posterior)</dt> </dl> |



 

 




