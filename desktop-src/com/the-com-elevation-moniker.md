---
title: O moniker de elevação COM
description: O moniker de elevação COM permite que os aplicativos que estão sendo executados no controle de conta de usuário (UAC) ativem classes COM com privilégios elevados. Para obter mais informações, consulte concentre-se no privilégio mínimo.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454395"
---
# <a name="the-com-elevation-moniker"></a>O moniker de elevação COM

O moniker de elevação COM permite que os aplicativos que estão sendo executados no controle de conta de usuário (UAC) ativem classes COM com privilégios elevados. Para obter mais informações, consulte [concentre-se no privilégio mínimo](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).

## <a name="when-to-use-the-elevation-moniker"></a>Quando usar o moniker de elevação

O moniker de elevação é usado para ativar uma classe COM para realizar uma função específica e limitada que exige privilégios elevados, como alterar a data e a hora do sistema.

A elevação requer a participação de uma classe COM e seu cliente. A classe COM deve ser configurada para dar suporte à elevação anotando sua entrada de registro, conforme descrito na seção requisitos. O cliente COM deve solicitar elevação usando o moniker de elevação.

O moniker de elevação não se destina a fornecer compatibilidade de aplicativos. Por exemplo, se você quiser executar um aplicativo COM herdado, como o WinWord como um servidor COM privilégios elevados, deverá configurar o executável do cliente COM para exigir elevação, em vez de ativar a classe do aplicativo herdado com o moniker de elevação. Quando o cliente COM elevado chama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usando o CLSID do aplicativo herdado, o estado elevado do cliente flui para o processo do servidor.

Nem todas as funcionalidades COM são compatíveis com a elevação. A funcionalidade que não funcionará inclui:

-   A elevação não flui de um cliente para um servidor COM remoto. Se um cliente ativar um servidor COM remoto com o moniker de elevação, o servidor não será elevado, mesmo que ele ofereça suporte à elevação.
-   Se uma classe COM privilegiada usar a representação durante uma chamada COM, poderá perder seus privilégios elevados durante a representação.
-   Se um servidor COM elevado registrar uma classe na corrompidos (tabela de objetos em execução), a classe não estará disponível para clientes não elevados.
-   Um processo elevado usando o mecanismo UAC não carrega classes por usuário durante ativações COM. Para aplicativos COM, isso significa que as classes COM do aplicativo devem ser instaladas no hive do registro do **\_ \_ computador local hKey** se o aplicativo for usado por contas sem privilégios e privilegiadas. As classes COM do aplicativo só precisam ser instaladas no hive de **\_ usuários do hKey** se o aplicativo nunca for usado por contas com privilégios.
-   O recurso arrastar e soltar não é permitido de aplicativos não elevados para elevados.

## <a name="requirements"></a>Requisitos

Para usar o moniker de elevação para ativar uma classe COM, a classe deve ser configurada para ser executada como o usuário de inicialização ou a identidade de aplicativo ' Activate as Activator '. Se a classe estiver configurada para ser executada sob qualquer outra identidade, a ativação retornará o valor de erro de CO \_ E \_ runas \_ \_ deve \_ ser \_ AAA.

A classe também deve ser anotada com um nome de exibição "amigável" que é compatível com MUI (Multilingual User interface). Isso requer a seguinte entrada de registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Se essa entrada estiver ausente, a ativação retornará o erro CO \_ E \_ faltando \_ DISPLAYNAME. Se o arquivo MUI estiver ausente, o código de erro da função [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) será retornado.

Opcionalmente, para especificar um ícone de aplicativo a ser exibido pela interface do usuário do UAC, adicione a seguinte chave do registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** usa o mesmo formato que a **localizadastring**:

@*pathtobinary*,*-resourcenumber*

Além disso, o componente COM deve ser assinado para que o ícone seja exibido.

A classe COM também deve ser anotada como habilitada para LUA. Isso requer a seguinte entrada de registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Se essa entrada estiver ausente, a ativação retornará o erro CO \_ E \_ elevação \_ desabilitada.

Observe que essas entradas devem existir no hive do \_ computador local hKey \_ , não no \_ Hive HKEY Current \_ User ou HKEY \_ users. Isso impede que os usuários elevem classes COM que não tenham também os privilégios de registro.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>O moniker de elevação e a interface do usuário de elevação

Se o cliente já estiver elevado, usar o moniker de elevação não fará com que a interface do usuário de elevação seja exibida.

## <a name="how-to-use-the-elevation-moniker"></a>Como usar o moniker de elevação

O moniker de elevação é um moniker COM padrão, semelhante aos monikers de sessão, partição ou fila. Ele direciona uma solicitação de ativação para um servidor especificado com o nível de elevação especificado. O CLSID a ser ativado aparece na cadeia de caracteres do moniker.

O moniker de elevação dá suporte aos seguintes tokens de nível de execução:

1.  Administrador
2.  O mais alto

A sintaxe para isso é a seguinte:

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

A sintaxe anterior usa o moniker "New" para retornar uma instância da classe COM especificada pelo *GUID*. Observe que o moniker "New" usa internamente a interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) para obter um objeto de classe e, em seguida, chama [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) nele.

O moniker de elevação também pode ser usado para obter um objeto de classe, que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Em seguida, o chamador chama [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para obter uma instância de objeto. A sintaxe para isso é a seguinte:

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Código de exemplo

O exemplo de código a seguir mostra como usar o moniker de elevação. Ele pressupõe que você já tenha inicializado COM no thread atual.


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



[**Associar \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) é novo no Windows Vista. Ele é derivado de [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).

A única adição é um campo **HWND** , **HWND**. Esse identificador representa uma janela que se torna o proprietário da interface do usuário de elevação, se aplicável.

Se **HWND** for **NULL**, com chamará [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) para localizar um identificador de janela associado ao thread atual. Esse caso pode ocorrer se o cliente for um script, que não pode preencher uma [**estrutura \_ OPTS3 do BIND**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) . Nesse caso, COM tentará usar a janela associada ao thread de script.

## <a name="over-the-shoulder-ots-elevation"></a>Elevação OTS (over-the-tiracolo)

A elevação OTS (over-the-tiracolo) refere-se ao cenário no qual um cliente executa um servidor com com as credenciais de um administrador, em vez de sua própria. (O termo "ao longo do ressalto" significa que o administrador está observando o ressalto do cliente enquanto o cliente executa o servidor.)

Esse cenário pode causar um problema para chamadas COM no servidor, porque o servidor pode não chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitamente (ou seja, de forma programática) ou implicitamente (ou seja, declarativamente, usando o registro). Para esses servidores, COM computa um descritor de segurança que permite que somente administradores de si, de sistema e internos façam \\ chamadas com no servidor. Essa organização não funcionará em cenários OTS. Em vez disso, o servidor deve chamar **CoInitializeSecurity**, explicitamente ou implicitamente, e especificar uma ACL que inclua o SID do grupo interativo e o System.

O exemplo de código a seguir mostra como criar um descritor de segurança (SD) com o SID do grupo interativo.

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

O exemplo de código a seguir mostra como chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitamente com o SD do exemplo de código anterior:


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



O exemplo de código a seguir mostra como chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitamente com o SD acima:


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a>Permissões COM e rótulos de acesso obrigatórios

O Windows Vista apresenta a noção de *Rótulos de acesso obrigatórios* em descritores de segurança. O rótulo determina se os clientes podem obter acesso de execução a um objeto COM. O rótulo é especificado na parte SACL (lista de controle de acesso) do sistema do descritor de segurança. No Windows Vista, o COM dá suporte ao \_ rótulo obrigatório do sistema \_ \_ nenhum \_ \_ rótulo de execução. As SACLs nas permissões COM são ignoradas em sistemas operacionais anteriores ao Windows Vista.

A partir do Windows Vista, dcomcnfg.exe não dá suporte à alteração do nível de integridade (IL) em permissões COM. Ele deve ser definido programaticamente.

O exemplo de código a seguir mostra como criar um descritor de segurança com um rótulo que permite solicitações de inicialização/ativação de todos os clientes de IL baixo. Observe que os rótulos são válidos para permissões de inicialização/ativação e chamada. Portanto, é possível gravar um servidor COM que não permita inicialização, ativação ou chamadas de clientes com um determinado IL. Para obter mais informações sobre os níveis de integridade, consulte a seção "entendendo o mecanismo de integridade do Windows Vista" em [compreendendo e trabalhando no modo protegido do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a>Níveis de CoCreateInstance e integridade

O comportamento de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) foi alterado no Windows Vista, para evitar que clientes de Il baixo sejam vinculados a servidores com por padrão. O servidor deve permitir explicitamente essas associações especificando a SACL. As alterações em **CoCreateInstance** são as seguintes:

1.  Ao iniciar um processo de servidor COM, o IL no token de processo do servidor é definido como o IL do token do cliente ou do servidor, o que for menor.
2.  Por padrão, o COM impedirá que clientes de IL baixo se vinculem às instâncias em execução de qualquer servidor COM. Para permitir a associação, o descritor de segurança de inicialização/ativação do servidor COM deve conter uma SACL que especifica o rótulo de IL baixo (consulte a seção anterior do código de exemplo para criar um descritor de segurança desse tipo).

## <a name="elevated-servers-and-rot-registrations"></a>Servidores elevados e registros corrompidos

Se um servidor COM quiser se registrar na corrompidos (tabela de objetos em execução) e permitir que qualquer cliente acesse o registro, ele deverá usar o \_ sinalizador ROTFLAGS ALLOWANYCLIENT. Um servidor COM "Activate as Activator" não pode especificar ROTFLAGS \_ ALLOWANYCLIENT porque o DCOMSCM (Gerenciador de controle de serviço) do DCOM impõe uma verificação de falsificação nesse sinalizador. Portanto, no Windows Vista, COM adiciona suporte para uma nova entrada de registro que permite ao servidor estipular que seus registros CORROMPIDOSs serão disponibilizados para qualquer cliente:

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

O único valor válido para essa \_ entrada reg DWORD é:

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

A entrada deve existir no hive **do \_ \_ computador local hKey** .

Essa entrada fornece um servidor "Activate as Activator" com a mesma funcionalidade que o ROTFLAGS \_ ALLOWANYCLIENT fornece para um servidor runas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> <dt>

[Compreendendo e trabalhando no Modo Protegido do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 