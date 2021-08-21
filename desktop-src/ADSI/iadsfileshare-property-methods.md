---
title: Métodos de propriedade IADsFileShare (IADs. h)
description: Os métodos de propriedade da interface IADsFileshare obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsFileShare
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6daec9905990d0f5cc5826b82b5361e0fc0653fafb0c617633a34b87c7a0e995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691414"
---
# <a name="iadsfileshare-property-methods"></a>Métodos de propriedade IADsFileShare

Os métodos de propriedade da interface [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**CurrentUserCount**
</dt> <dd> <dl>

O número de usuários conectados ao compartilhamento.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

**Descrição**
</dt> <dd> <dl>

A descrição do compartilhamento de arquivos.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

Uma referência de ADsPath para o computador host.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

**MaxUserCount**
</dt> <dd> <dl>

O número máximo de usuários com permissão para acessar o compartilhamento ao mesmo tempo.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

**Caminho**
</dt> <dd> <dl>

O caminho do sistema de arquivos para o diretório compartilhado.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

Para acessar as propriedades de compartilhamentos de arquivos em um computador, você deve primeiro ligar a "LanmanServer" no computador. O exemplo de código a seguir mostra como configurar a descrição e o número máximo de usuários permitidos para todos os compartilhamentos de arquivos públicos no computador, nomeados como "mymachine", no domínio padrão.


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



O exemplo de código a seguir mostra como tornar o diretório C: \\ MyFolder existente um compartilhamento de arquivo público.


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



O exemplo de código a seguir torna o diretório C: \\ MyFolder existente um compartilhamento de arquivo público.


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsFileShare é definido como EB6DCAF0-4B83-11CF-A995-00AA006BC149<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

 





