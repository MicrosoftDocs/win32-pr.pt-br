---
description: Instala um pacote de exceção.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Função InstallComponentW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749865"
---
# <a name="installcomponentw-function"></a>Função InstallComponentW

Instala um pacote de exceção.

## <a name="syntax"></a>Sintaxe


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InfPath* \[ no\]
</dt> <dd>

O caminho para o INF de exceção a ser processado.

</dd> <dt>

*CompGuid* \[ em, opcional\]
</dt> <dd>

O GUID do componente de exceção que está sendo instalado.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Os sinalizadores usados para controlar os comportamentos de instalação. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                               | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**Comp \_ SINALIZADORES/ \_ força**</dt> <dt>0x00000020</dt> </dl>                             | Ignora a verificação de versão nas substituições de arquivo.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**Comp \_ os sinalizadores \_ precisam ser \_ desinstalados**</dt><dt></dt> </dl>        | Faça backup de arquivos que são atualizados para serem usados por uma desinstalação do componente.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**Comp \_ SINALIZADORES \_ sem \_ substituição**</dt><dt></dt> </dl>                 | Ignora o backup de arquivos se a versão do componente de exceção é igual a um componente instalado. Esse sinalizador é usado em um cenário de reinstalação.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**Comp \_ SINALIZADORES \_ NOUI**</dt> <dt>0x00000002</dt> </dl>                                | Suprime toda a interface do usuário.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**Comp \_ SINALIZADORES de \_ atualização de \_ dllcache**</dt><dt></dt> </dl>        | Força o diretório DLLCACHE a ser atualizado quando um arquivo do sistema é atualizado.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**Comp \_ SINALIZADORES \_ usam \_ \_ cache Svcpack**</dt><dt></dt> </dl> | Usa arquivos armazenados em cache por um Windows service pack instalar para substituir arquivos submetidos a backup.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ em, opcional\]
</dt> <dd>

A versão principal do componente de exceção.

</dd> <dt>

*Verminor* \[ em, opcional\]
</dt> <dd>

A versão secundária do componente de exceção.

</dd> <dt>

*VerBuild* \[ em, opcional\]
</dt> <dd>

A versão de compilação do componente de exceção.

</dd> <dt>

*VerQFE* \[ em, opcional\]
</dt> <dd>

A revisão do hotfix do componente de exceção.

</dd> <dt>

*Nome* \[ do em, opcional\]
</dt> <dd>

A cadeia de caracteres descritiva do componente mostrado pela caixa de diálogo proteção de arquivo do Windows se o sistema operacional detectar que um arquivo protegido de proteção de arquivo do Windows está danificado, adulterado ou corrompido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna um valor **HRESULT** (S \_ OK ou um código de falha). Um código de falha pode ser verificado em relação a um valor de 0x20000100 para determinar se a falha ocorre porque uma reinicialização é necessária.

## <a name="remarks"></a>Comentários

Os pacotes de exceção são arquivos de sistema do Windows que são liberados fora de uma versão completa do Windows do pacote e que atualizam os arquivos do sistema operacional. Os pacotes de exceção são criados somente por equipes de sistema operacional que receberam autorização para atualizar os arquivos de sistema do Windows.

Para instalar e desinstalar arquivos que não são protegidos pela proteção de arquivos do Windows, use as funções documentadas em [funções gerais de instalação](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar drivers de dispositivo, os dispositivos de vendas devem usar funções documentadas em [funções de instalação de dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e funções de [Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
