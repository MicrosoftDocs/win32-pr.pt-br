---
title: Método ITSRemoteProgram ServerStartProgram
description: Especifica um programa do RemoteApp para iniciar na sessão remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota, interface ITSRemoteProgram
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram, método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota, interface ITSRemoteProgram2
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram2, método ServerStartProgram
- Método ServerStartProgram Serviços de Área de Trabalho Remota, interface ITSRemoteProgram3
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram3, método ServerStartProgram
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
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499463"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>Método ITSRemoteProgram:: ServerStartProgram

Especifica um programa do RemoteApp para iniciar na sessão remota. Essa função deve ser invocada em uma sessão conectada (depois que a notificação de sessão conectada for recebida no cliente). Qualquer número de programas do RemoteApp pode ser iniciado em uma sessão. Uma sessão do RemoteApp atingirá o tempo limite se nenhum programa do RemoteApp for iniciado na sessão dentro do limite de tempo limite, que é de dois minutos para o Windows Server 2008.

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

*bstrExecutablePath* \[ no\]
</dt> <dd>

O caminho do arquivo executável do programa do RemoteApp no servidor.

</dd> <dt>

*bstrFilePath* \[ no\]
</dt> <dd>

O caminho de um arquivo a ser aberto no servidor por meio de uma associação de arquivo, por exemplo, "C: \\ \\ documents \\ \\MyReport.docx". Se você especificar *bstrFilePath*, não deverá especificar o parâmetro *bstrExecutablePath* e vice-versa. Você deve especificar apenas um dos parâmetros.

</dd> <dt>

*bstrWorkingDirectory* \[ no\]
</dt> <dd>

O diretório de trabalho no servidor para o programa RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ no\]
</dt> <dd>

Indica se o servidor deve expandir as variáveis de ambiente no caminho do diretório de trabalho. Defina esse parâmetro como **Variant \_ true** se o caminho do diretório de trabalho contiver variáveis de ambiente ou **Variant \_ false** se o caminho do diretório de trabalho não contiver variáveis de ambiente.

</dd> <dt>

*bstrArguments* \[ no\]
</dt> <dd>

Os argumentos de linha de comando para o programa RemoteApp que são especificados em *bstrExecutablePath*. Defina como **NULL** se *bstrExecutablePath* não for especificado.

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ no\]
</dt> <dd>

Indica se o servidor deve expandir as variáveis de ambiente nos argumentos de linha de comando. Defina esse parâmetro como **Variant \_ true** se os argumentos contiverem variáveis de ambiente ou **Variant \_ false** se os argumentos não contiverem variáveis de ambiente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram é definido como FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





