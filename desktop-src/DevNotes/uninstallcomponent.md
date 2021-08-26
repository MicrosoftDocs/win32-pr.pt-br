---
description: Remove um pacote de exceção.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Função UninstallComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: d6b4ce8e447bc884d1b3ee64505d230b2e069ce6cda1630b027b8a48da68beda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001106"
---
# <a name="uninstallcomponent-function"></a>Função UninstallComponent

Remove um pacote de exceção.

## <a name="syntax"></a>Sintaxe


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CompGuid* \[ in, opcional\]
</dt> <dd>

O GUID do componente de exceção que está sendo desinstalado.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Os sinalizadores usados para controlar os comportamentos de instalação. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                         | Significado                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**NOUI \_ DE SINALIZADORES DE COMP \_**</dt> </dl>                                          | Suprime toda a interface do usuário.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**\_ \_ DLLCACHE DE ATUALIZAÇÃO DE SINALIZADORES DO COMP \_**</dt> </dl>        | Força o diretório DLLCACHE a ser atualizado quando um arquivo do sistema é atualizado.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**SINALIZADORES \_ COMP USAM O \_ \_ CACHE SVCPACK \_**</dt> </dl> | Usa arquivos armazenados em cache por um Windows service pack instalados para sobressusar o backup de arquivos.<br/> |



 

</dd> <dt>

*VerMajor* \[ in, opcional\]
</dt> <dd>

A versão principal do componente Exception a ser desinstalado.

</dd> <dt>

*VerMinor* \[ in, opcional\]
</dt> <dd>

A versão secundária do componente Exception a ser desinstalada.

</dd> <dt>

*VerBuild* \[ in, opcional\]
</dt> <dd>

A versão de build do componente Exception a ser desinstalada.

</dd> <dt>

*VerQFE* \[ in, opcional\]
</dt> <dd>

A revisão de hotfix do componente Exception a ser desinstalado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Os pacotes de exceção Windows arquivos do sistema que são liberados fora de um pacote completo Windows versão e que atualizem arquivos do sistema operacional. Os pacotes de exceção são escritos somente por equipes do sistema operacional que recebeu autorização para atualizar Windows do sistema.

Para instalar e desinstalar arquivos que não são protegidos pelo Windows Proteção de Arquivos, use as funções documentadas em Funções de [Instalação Geral](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar drivers de dispositivo, os revendedores devem usar funções documentadas em Funções de Instalação do Dispositivo e [](https://msdn.microsoft.com/library/ms792954.aspx) [PnP Gerenciador de Configurações Functions](https://msdn.microsoft.com/library/ms790838.aspx).

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 
