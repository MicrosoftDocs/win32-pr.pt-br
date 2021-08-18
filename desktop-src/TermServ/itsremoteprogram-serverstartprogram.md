---
title: Método ITSRemoteProgram ServerStartProgram
description: Especifica um programa RemoteApp para iniciar na sessão remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Método ServerStartProgram Serviços de Área de Trabalho Remota
- Método ServerStartProgram Serviços de Área de Trabalho Remota , interface ITSRemoteProgram
- Interface ITSRemoteProgram Serviços de Área de Trabalho Remota , método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota , interface ITSRemoteProgram2
- Interface ITSRemoteProgram2 Serviços de Área de Trabalho Remota , método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota , interface ITSRemoteProgram3
- Interface ITSRemoteProgram3 Serviços de Área de Trabalho Remota , método ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c789a9963086128e93546415247cfb3db69afe59c67a445b851ee5cf3687d16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756852"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>Método ITSRemoteProgram::ServerStartProgram

Especifica um programa RemoteApp para iniciar na sessão remota. Essa função deve ser invocada em uma sessão conectada (depois que a notificação conectada da sessão for recebida no cliente). Qualquer número de programas RemoteApp pode ser iniciado em uma sessão. Uma sessão do RemoteApp terá o tempo limite se nenhum programa RemoteApp for iniciado na sessão dentro do limite de tempo limite, que é de dois minutos para Windows Server 2008.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrExecutablePath* \[ Em\]
</dt> <dd>

O caminho do arquivo executável do programa RemoteApp no servidor.

</dd> <dt>

*bstrFilePath* \[ Em\]
</dt> <dd>

O caminho de um arquivo a ser aberto no servidor por meio de uma associação de arquivo, por exemplo"C: \\ \\ Documentos \\ \\MyReport.docx". Se você especificar *bstrFilePath*, não deverá especificar o *parâmetro bstrExecutablePath* e vice-versa. Você deve especificar apenas um dos parâmetros.

</dd> <dt>

*bstrWorkingDirectory* \[ Em\]
</dt> <dd>

O diretório de trabalho no servidor do programa RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ Em\]
</dt> <dd>

Indica se o servidor deve expandir variáveis de ambiente no caminho do diretório de trabalho. De definir esse parâmetro como **VARIANT \_ TRUE** se o caminho do diretório de trabalho contiver variáveis de ambiente ou **VARIANT \_ FALSE** se o caminho do diretório de trabalho não contiver variáveis de ambiente.

</dd> <dt>

*bstrArguments* \[ Em\]
</dt> <dd>

Os argumentos de linha de comando para o programa RemoteApp especificados em *bstrExecutablePath*. De definido como **NULL** *se bstrExecutablePath* não for especificado.

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ Em\]
</dt> <dd>

Indica se o servidor deve expandir variáveis de ambiente nos argumentos de linha de comando. De definir esse parâmetro como **VARIANT \_ TRUE** se os argumentos contêm variáveis de ambiente ou **VARIANT \_ FALSE** se os argumentos não contêm variáveis de ambiente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram é definido como \_ FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





