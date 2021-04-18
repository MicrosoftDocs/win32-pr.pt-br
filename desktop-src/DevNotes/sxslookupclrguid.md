---
description: Recupera o nome da classe e outras informações associadas a um determinado GUID no manifesto de um componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Função SxsLookupClrGuid
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751348"
---
# <a name="sxslookupclrguid-function"></a>Função SxsLookupClrGuid

Recupera o nome da classe e outras informações associadas a um determinado GUID no manifesto de um componente. Essa função é usada somente ao implementar a interoperabilidade gerenciada e não gerenciada de baixo nível no .NET Framework. Para obter mais informações sobre a interoperabilidade gerenciada não gerenciada, consulte "interoperação com código não gerenciado" no SDK do .NET Framework e também [aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

## <a name="syntax"></a>Sintaxe


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Uma combinação de zero ou mais dos sinalizadores a seguir.



| Valor                                                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ use \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Se esse sinalizador for definido, o parâmetro *hActCtx* deverá conter um identificador de contexto de ativação retornado pela função [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Se esse sinalizador não for definido, o parâmetro *hActCtx* será ignorado e **SxsLookupClrGuid** pesquisará o contexto de ativação que está ativo no momento (a função [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) é usada para tornar um contexto de ativação ativo).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ localizar \_**</dt> <dt>0x00010000</dt> substituto </dl>  | Se esse sinalizador for definido, o **SxsLookupClrGuid** pesquisará um substituto.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ localizar \_ \_ classe CLR**</dt> <dt>0x00020000</dt> </dl> | Se esse sinalizador for definido, **SxsLookupClrGuid** pesquisará uma classe.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ localizar \_ qualquer**</dt> <dt>0x00030000</dt> </dl>                    | Essa é uma combinação do **GUID de pesquisa de SxS de \_ \_ CRL \_ \_ localizar \_ substituto** e **SxS \_ pesquisador de CLR localizar sinalizadores de \_ \_ \_ \_ \_ classe CLR** ; se ambos estiverem definidos, **SxsLookupClrGuid** procurará um substituto primeiro e somente se ele não encontrar um, então procurará uma classe.<br/>                                                                                                                                                |



 

</dd> <dt>

*pCLSID* \[ no\]
</dt> <dd>

Um ponteiro para o GUID sobre o qual Pesquisar as informações de interoperação no contexto de ativação. Este parâmetro não pode ser **nulo**.

</dd> <dt>

*hActCtx* \[ em, opcional\]
</dt> <dd>

Se o **\_ GUID CLR de pesquisa de SxS \_ \_ \_ usar \_** o sinalizador ACTCTX estiver definido no parâmetro *dwFlags* , *hActCtx* deverá conter um identificador de contexto de ativação retornado pela função [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Caso contrário, *hActCtx* será ignorado.

</dd> <dt>

*pvOutputBuffer* \[ entrada, saída, opcional\]
</dt> <dd>

Ponteiro para o buffer no qual as informações de retorno são copiadas. Esse parâmetro pode ser de valor nulo somente se o parâmetro *cbOutputBuffer* tiver valor zero. Os dados colocados nesse buffer na saída (se houver) consistem em uma **estrutura \_ \_ \_ CLR de informações de GUID SxS** seguida por quaisquer dados de cadeia de caracteres adicionais necessários. Consulte a seção comentários abaixo para obter mais informações.

</dd> <dt>

*cbOutputBuffer* \[ no\]
</dt> <dd>

Tamanho em bytes do buffer apontado pelo parâmetro *pvOutputBuffer* .

</dd> <dt>

*pcbOutputBuffer* \[ fora\]
</dt> <dd>

Ponteiro para uma variável em que o tamanho, em bytes, das informações de retorno é colocado na saída. Se o parâmetro *cbOutputBuffer* for zero ou se o tamanho do buffer de saída for menor do que o tamanho das informações de retorno, **SxsLookupClrGuid** falhará e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de **\_ \_ buffer insuficiente**. Nesse caso, use o valor na variável apontada por *pcbOutputBuffer* para alocar um buffer grande o suficiente e, em seguida, chame **SxsLookupClrGuid** novamente para recuperar as informações desejadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário. Para obter mais informações de erro, chame [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Os componentes gerenciados podem se declarar como suporte a "assemblies de interoperabilidade" gerenciados para permitir que um consumidor de componente Win32 não gerenciado referencie o assembly declarativo. O consumidor do componente pode interagir com o componente gerenciado chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em um GUID. A camada de interoperação roteia a solicitação de criação de objeto para .NET Framework, cria uma instância do objeto gerenciado e retorna um ponteiro de interface.

O **SxsLookupClrGuid** permite que as estruturas recuperem informações associadas a um determinado GUID no manifesto do componente, como o que é o nome da classe .net, qual versão do .NET Framework ela requer e em qual assembly host ele está localizado. Os componentes gerenciados publicam um assembly de interoperabilidade que contém várias instruções que associam GUIDs com nomes de assembly e de tipo, e os agentes de tempo de execução do .NET a construção de instâncias de objeto gerenciado quando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é chamado.

Veja a seguir um manifesto de componente de exemplo declarando um GUID CLR e um substituto CLR que o **SxsLookupClrGuid** pode Pesquisar:

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

Um provedor de interoperação chamaria **SxsLookupClrGuid** com um ponteiro para o GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" e receberia, em seguida, retornará o nome de classe "MySampleSurrogate", a versão de tempo de execução necessária "1.0.3055" e a identidade textual "dotnet. Sample. substitutos, versão = ' 1.0.0.0 ', tipo = ' Interop '" do componente de hospedagem.

Essas informações de retorno seriam contidas e/ou referenciadas por uma estrutura do **\_ CLR de \_ informações \_ de GUID SxS** declarada da seguinte maneira.

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

Os membros dessa estrutura contêm as informações a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro</th>
<th>DESCRIÇÃO</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br/></td>
<td>Contém o tamanho da estrutura de SXS_GUID_INFORMATION_CLR (isso permite que a estrutura cresça em versões posteriores).<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br/></td>
<td>Contém um dos dois valores de sinalizador a seguir: <br/>
<ul>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica que o GUID especificado foi associado a um &quot; substituto.&quot;</li>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica que o GUID especificado foi associado a uma &quot; classe.&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br/></td>
<td>Aponta para uma cadeia de caracteres largo com terminação zero que identifica a versão do tempo de execução especificado no manifesto do host para essa classe.<br/></td>
</tr>
<tr class="even">
<td><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br/></td>
<td>Aponta para uma cadeia de caracteres largo com terminação zero que contém o nome da classe .NET associada ao GUID especificado.<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br/></td>
<td>Aponta para uma cadeia de caracteres largo com terminação zero que contém a identidade textual do assembly que hospeda essa classe. Para obter mais informações sobre a identidade textual, consulte &quot; especificando nomes de tipos totalmente qualificados &quot; em &quot; descobrindo informações de tipo em tempo de execução &quot; em &quot; programação com o .NET Framework &quot; no SDK do .NET Framework.<br/></td>
</tr>
</tbody>
</table>



 

Um aplicativo não gerenciado pode usar as informações retornadas dessa maneira para carregar a versão correta do .NET Framework, carregar o assembly identificado pelo elemento **pcwszAssemblyIdentity** e, em seguida, criar uma instância da classe nomeada pelo elemento **pcwszTypeName** .

## <a name="examples"></a>Exemplos

Use a vinculação dinâmica da seguinte maneira para chamar a função **SxsLookupClrGuid** :


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
