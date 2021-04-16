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
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751376"
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

*CompGuid* \[ em, opcional\]
</dt> <dd>

O GUID do componente de exceção que está sendo desinstalado.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Os sinalizadores usados para controlar os comportamentos de instalação. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                         | Significado                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**sinalizadores de COMP \_ \_ NOUI**</dt> </dl>                                          | Suprime toda a interface do usuário.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**sinalizadores de COMP \_ \_ Atualizar \_ dllcache**</dt> </dl>        | Força o diretório DLLCACHE a ser atualizado quando um arquivo do sistema é atualizado.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**os \_ sinalizadores de comp \_ usam o \_ \_ cache Svcpack**</dt> </dl> | Usa arquivos armazenados em cache por um Windows service pack instalar para substituir arquivos submetidos a backup.<br/> |



 

</dd> <dt>

*VerMajor* \[ em, opcional\]
</dt> <dd>

A versão principal do componente de exceção a ser desinstalada.

</dd> <dt>

*Verminor* \[ em, opcional\]
</dt> <dd>

A versão secundária do componente de exceção a ser desinstalada.

</dd> <dt>

*VerBuild* \[ em, opcional\]
</dt> <dd>

A versão de compilação do componente de exceção a ser desinstalada.

</dd> <dt>

*VerQFE* \[ em, opcional\]
</dt> <dd>

A revisão do hotfix do componente de exceção a ser desinstalado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Os pacotes de exceção são arquivos de sistema do Windows que são liberados fora de uma versão completa do Windows do pacote e que atualizam os arquivos do sistema operacional. Os pacotes de exceção são criados somente por equipes de sistema operacional que receberam autorização para atualizar os arquivos de sistema do Windows.

Para instalar e desinstalar arquivos que não são protegidos pela proteção de arquivos do Windows, use as funções documentadas em [funções gerais de instalação](https://msdn.microsoft.com/library/ms794585.aspx). Para instalar drivers de dispositivo, os dispositivos de vendas devem usar funções documentadas em [funções de instalação de dispositivo](https://msdn.microsoft.com/library/ms792954.aspx) e funções de [Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 
