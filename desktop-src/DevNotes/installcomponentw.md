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
ms.openlocfilehash: 9deaa460ec58ad0aa07af38aa03f53971068b4a6a1d43131e5473a7e4def908c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955915"
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

*InfPath* \[ Em\]
</dt> <dd>

O caminho para a exceção INF a ser processado.

</dd> <dt>

*CompGuid* \[ in, opcional\]
</dt> <dd>

O GUID do componente de exceção que está sendo instalado.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Os sinalizadores usados para controlar os comportamentos de instalação. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                               | Significado                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_ SINALIZADORES \_ FORCE**</dt> <dt>0X00000020</dt> </dl>                             | Ignora a verificação de versão em substituições de arquivo.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_ OS SINALIZADORES \_ PRECISAM SER \_ DESINSTALADOS**</dt><dt></dt> </dl>        | Fazer o back-up de arquivos que são atualizados para serem usados por uma desinstalação do componente.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_ SINALIZADORES \_ \_ SEM SUBSTITUIR**</dt><dt></dt> </dl>                 | Ignora o back-up de arquivos se a versão do componente Exception for a mesma que um componente instalado. Esse sinalizador é usado em um cenário de reinstalação.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ SINALIZADORES \_ NOUI**</dt> <dt>0x00000002</dt> </dl>                                | Suprime toda a interface do usuário.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ FLAGS \_ UPDATE \_ DLLCACHE**</dt><dt></dt> </dl>        | Força o diretório DLLCACHE a ser atualizado quando um arquivo do sistema é atualizado.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_ SINALIZADORES \_ USAM \_ CACHE \_ SVCPACK**</dt><dt></dt> </dl> | Usa arquivos armazenados em cache por um Windows service pack instalados para sobressusar o backup de arquivos.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, opcional\]
</dt> <dd>

A versão principal do componente Exception.

</dd> <dt>

*VerMinor* \[ in, opcional\]
</dt> <dd>

A versão secundária do componente Exception.

</dd> <dt>

*VerBuild* \[ in, opcional\]
</dt> <dd>

A versão de build do componente Exception.

</dd> <dt>

*VerQFE* \[ in, opcional\]
</dt> <dd>

A revisão de hotfix do componente Exception.

</dd> <dt>

*Nome* \[ in, opcional\]
</dt> <dd>

A cadeia de caracteres descritiva do componente mostrada pela caixa de diálogo Windows Proteção de Arquivos do Windows se o sistema operacional detectar que um arquivo de proteção de arquivos Windows está danificado, adulterado ou corrompido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna um **valor HRESULT** (S \_ OK ou um código de falha). Um código de falha pode ser verificado em relação a um valor de 0x20000100 para determinar se a falha é porque uma reinicialização é necessária.

## <a name="remarks"></a>Comentários

Os pacotes de exceção Windows arquivos do sistema que são liberados fora de um pacote completo Windows versão e que atualizem arquivos do sistema operacional. Os pacotes de exceção são escritos somente por equipes do sistema operacional que recebeu autorização para atualizar Windows do sistema.

Para instalar e desinstalar arquivos que não são protegidos pelo Windows Proteção de Arquivos, use as funções documentadas em Funções de [Instalação Geral](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar drivers de dispositivo, os revendedores devem usar funções documentadas em Funções de Instalação do Dispositivo e [](https://msdn.microsoft.com/library/ms792954.aspx) [PnP Gerenciador de Configurações Functions](https://msdn.microsoft.com/library/ms790838.aspx).

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
