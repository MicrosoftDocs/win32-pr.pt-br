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
ms.openlocfilehash: 516ba97eb70defdbc6f92efa5c65e6d23246fe67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465593"
---
# <a name="sxslookupclrguid-function"></a>Função SxsLookupClrGuid

Recupera o nome da classe e outras informações associadas a um determinado GUID no manifesto de um componente. Essa função é usada somente ao implementar a interoperabilidade gerenciada não gerenciada de baixo nível no .NET Framework. Para obter mais informações sobre interoperabilidade gerenciada não gerenciada, consulte "Interoperação com código não gerenciado" no SDK do .NET Framework e também Aplicativos isolados e [assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)lado a lado.

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

*dwFlags* \[ Em\]
</dt> <dd>

Uma combinação de zero ou mais dos sinalizadores a seguir.



| Valor                                                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SXS \_ GUID DE \_ CLR \_ DE LOOKUP \_ USE \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Se esse sinalizador for definido, o parâmetro *hActCtx* deverá conter um handle de contexto de ativação retornado pela [**função CreateActCtx.**](/windows/win32/api/winbase/nf-winbase-createactctxa) Se esse sinalizador não estiver definido, o parâmetro *hActCtx* será ignorado e **SxsLookupClrGuid** pesquisa o contexto de ativação que está ativo no momento (a [**função ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) é usada para ativar um contexto de ativação).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SXS \_ GUID DO \_ CLR \_ LOOKUP \_ FIND \_ SURROGATE**</dt> <dt>0X00010000</dt> </dl>  | Se esse sinalizador estiver definido, **SxsLookupClrGuid** procurará um substituto.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SXS \_ CLASSE \_ DE \_ \_ CLR FIND \_ CLR \_ GUID LOOKUP 0X00020000**</dt> <dt></dt> </dl> | Se esse sinalizador estiver definido, **SxsLookupClrGuid** pesquisa uma classe.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SXS \_ GUID DO \_ CLR \_ DE LOOKUP \_ ENCONTRAR \_ QUALQUER**</dt> <dt>0X00030000</dt> </dl>                    | Essa é uma combinação dos sinalizadores DE CLASSE CLR FIND SURROGATE e **SXS \_ \_ \_ \_ \_ LOOKUP** **\_ \_ CLR \_ \_ \_ \_ GUID FIND;** se ambos estão definidos, **SxsLookupClrGuid** procura um substituto primeiro e, somente se ele não encontrar um, pesquisa uma classe.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ Em\]
</dt> <dd>

Um ponteiro para o GUID sobre o qual pesquisar informações de interoperação no contexto de ativação. Esse parâmetro não pode ser **NULL.**

</dd> <dt>

*hActCtx* \[ in, opcional\]
</dt> <dd>

Se o sinalizador **SXS \_ LOOKUP \_ CLR \_ GUID USE \_ \_ ACTCTX** estiver definido no parâmetro *dwFlags,* *hActCtx* deverá conter um handle de contexto de ativação retornado pela [**função CreateActCtx.**](/windows/win32/api/winbase/nf-winbase-createactctxa) Caso contrário, *hActCtx* será ignorado.

</dd> <dt>

*pvOutputBuffer* \[ in, out, opcional\]
</dt> <dd>

Ponteiro para o buffer no qual as informações de retorno são copiadas. Esse parâmetro poderá ter valor NULL somente se o *parâmetro cbOutputBuffer* tiver valor zero. Os dados colocados nesse buffer na saída (se algum) consistem em uma estrutura **\_ \_ \_ CLR** de INFORMAÇÕES DO GUID SXS seguida por quaisquer dados de cadeia de caracteres adicionais necessários. Consulte a seção Comentários abaixo para obter mais informações.

</dd> <dt>

*cbOutputBuffer* \[ Em\]
</dt> <dd>

Tamanho em bytes do buffer apontado pelo *parâmetro pvOutputBuffer.*

</dd> <dt>

*pcbOutputBuffer* \[ out\]
</dt> <dd>

Ponteiro para uma variável em que o tamanho, em bytes, das informações de retorno é colocado na saída. Se o parâmetro *cbOutputBuffer* for zero ou se o tamanho do buffer de saída for menor que o tamanho das informações de retorno, **SxsLookupClrGuid** falhará e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro **DE ERRO BUFFER \_ \_ INSUFICIENTE.** Nesse caso, use o valor na variável apontada por *pcbOutputBuffer* para alocar um buffer grande o suficiente e, em seguida, chame **SxsLookupClrGuid** novamente para recuperar as informações desejadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário. Para obter mais informações de erro, [ **chame GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Os componentes gerenciados podem se declarar como "assemblies de interop" gerenciados para permitir que um consumidor de componente Win32 não gerenciado referenciar o assembly declarativo. O consumidor do componente pode interagir com o componente gerenciado chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em um GUID. A camada de interoperação encaminha a solicitação de criação de objeto para .NET Framework, cria uma instância do objeto gerenciado e retorna um ponteiro de interface.

**SxsLookupClrGuid** permite que as estruturas recuperem informações associadas a um determinado GUID no manifesto do componente, como qual é seu nome de classe .NET, qual versão do .NET Framework ele requer e em qual assembly de host ele está localizado. Os componentes gerenciados publicam um assembly de interop que contém várias instruções associando GUIDs a nomes de assembly e tipo, e o runtime do .NET intermedia a construção de instâncias de objeto gerenciado quando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é chamado.

Veja a seguir um manifesto de componente de exemplo declarando um GUID CLR e um substituto CLR que **SxsLookupClrGuid** pode procurar:

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

Um provedor de interoperação chamaria **SxsLookupClrGuid** com um ponteiro para o GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", e receberiam em retornar o nome de classe "MySampleSurrogate", a versão de runtime necessária "1.0.3055" e a identidade textual "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" do componente de hospedagem.

Essas informações de retorno seriam contidas e/ou referenciadas por uma estrutura **\_ \_ \_ CLR** de INFORMAÇÕES DO GUID SXS declarada da seguinte forma.

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




| Membro | DESCRIÇÃO | 
|--------|-------------|
| <span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>Cbsize</strong><br /> | Contém o tamanho da estrutura SXS_GUID_INFORMATION_CLR (isso permite que a estrutura cresça em versões posteriores).<br /> | 
| <span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>Dwflags</strong><br /> | Contém um dos dois valores de sinalizador a seguir: <br /><ul><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica que o GUID especificado foi associado a um "substituto".</li><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica que o GUID especificado foi associado a uma "classe".</li></ul> | 
| <span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br /> | Aponta para uma cadeia de caracteres largos terminada em zero que identifica a versão do runtime especificada no manifesto do host para essa classe.<br /> | 
| <span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br /> | Aponta para uma cadeia de caracteres largos terminada em zero que contém o nome da classe .NET associada ao GUID especificado.<br /> | 
| <span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br /> | Aponta para uma cadeia de caracteres largos terminada em zero que contém a identidade textual do assembly que hospeda essa classe. Para obter mais informações sobre a identidade textual, consulte "Especificando nomes de tipo totalmente qualificados" em "Descobrindo informações de tipo em tempo de executar" em "Programando com o .NET Framework" no SDK do .NET Framework.<br /> | 




 

Um aplicativo nãomanagedo pode usar as informações retornadas dessa maneira para carregar a versão correta do .NET Framework, carregar o assembly identificado pelo elemento **pcwszAssemblyIdentity** e, em seguida, criar uma instância da classe chamada pelo elemento **pcwszTypeName.**

## <a name="examples"></a>Exemplos

Use a vinculação dinâmica da seguinte forma para chamar a **função SxsLookupClrGuid:**


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

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
