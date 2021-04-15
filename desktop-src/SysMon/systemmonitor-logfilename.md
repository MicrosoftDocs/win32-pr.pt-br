---
title: Propriedade SystemMonitor. LogFilename
description: Recupera ou define o nome de um arquivo de log a ser usado como a origem dos valores do contador exibidos no monitor do sistema.
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- Propriedade LogFilename SysMon
- Propriedade LogFilename SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Propriedade LogFilename
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369639"
---
# <a name="systemmonitorlogfilename-property"></a>Propriedade SystemMonitor. LogFilename

Recupera ou define o nome de um arquivo de log a ser usado como a origem dos valores do contador exibidos no monitor do sistema.

> [!Note]  
> Essa propriedade tornou-se obsoleta pela propriedade [**LogFiles**](systemmonitor-logfiles.md) .

 

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property LogFileName As String
```



## <a name="property-value"></a>Valor da propriedade

Caminho para o arquivo de log. Você pode especificar um caminho absoluto, relativo ou UNC. A extensão do nome do arquivo de log deve ser. csv,. tsv ou. blg.

## <a name="exceptions"></a>Exceções



| Tipo de exceção                                  | Condição                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | Não é possível localizar o arquivo especificado. O valor Err. Number é 0xC0000BD1. |
| **System. ArgumentException**                    | Você não pode especificar uma cadeia de caracteres vazia.                                    |



 

## <a name="remarks"></a>Comentários

Essa propriedade retorna o nome do arquivo de log do primeiro membro da coleção [**LogFiles**](systemmonitor-logfiles.md) .

A definição dessa propriedade falhará se a coleção [**LogFiles**](systemmonitor-logfiles.md) contiver um ou mais membros.

Você deve usar a ferramenta Logman.exe ou o snap-in do MMC Perfmon. msc para gerar os arquivos de log que você adiciona a essa coleção. Para Perfmon. msc, os logs de contador estão localizados em **logs e alertas de desempenho**. Para obter detalhes sobre como usar Logman.exe ou Perfmon. msc, pesquise logman ou usando o desempenho, respectivamente, no **centro de ajuda e suporte**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





