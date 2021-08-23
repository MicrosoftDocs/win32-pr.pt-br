---
description: Controle da instância do coletor. Requer os privilégios de administrador (BA).
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Classe de controle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5eeccd31f3d9ab1f0b0ec05ebf80ea9f880a73fed21b21fe67fe63257af28871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589016"
---
# <a name="control-class"></a>Classe de controle

Controle da instância do coletor. Requer os privilégios de administrador (BA).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>Membros

A classe **Control** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Control** tem esses métodos.



| Método                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ponto de verificação**](control-checkpoint.md)                       | Se a configuração atual for um resultado da função desfazer/refazer/restaurar, o marcará como se ela estivesse definida explicitamente, de modo que o histórico preservará a hora em que foi definido e um arquivo de backup será criado para ele na próxima alteração de configuração. Se a configuração atual já foi definida explicitamente, não terá efeito. Retorna 1 em caso de êxito, 0 em erro.<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | Despeje as informações de diagnóstico no log.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | Pare o coletor rapidamente, descartando todos os dados na fila.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Liberar**](control-flush.md)                                 | Libere os buffers do encaminhador.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Leia a configuração ativa do coletor.<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | Compare o argumento com a configuração ativa do coletor. Retornará 1 se eles corresponderem, 0 se não forem.<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | Retorne a lista dos arquivos de configuração de backup salvos que podem ser restaurados.<br/>                                                                                                                                                                                                                                                                                  |
| [**Refazer**](control-redo.md)                                   | Redefina a configuração ativa do coletor a partir do arquivo de backup posterior (determinado ao avançar do carimbo de data/hora original atual). Se a configuração tiver sido desfeita, isso significará refazer a alteração desfeita. Retorna 1 em caso de êxito, 0 em erro.<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | Restaure a configuração ativa do coletor de um arquivo de backup. Retorna 1 em caso de êxito, 0 em erro.<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | Restaure a configuração ativa do coletor de um arquivo de backup, selecionado por um carimbo de data/hora. Retorna 1 em caso de êxito, 0 em erro.<br/>                                                                                                                                                                                                                               |
| [**Configuração de**](control-setconfiguration.md)           | Defina a nova configuração ativa do coletor. Retorna 1 em caso de êxito, 0 em erro.<br/>                                                                                                                                                                                                                                                                           |
| [**Desligamento**](control-shutdown.md)                           | Pare o coletor. Se o coletor estiver sendo executado como um serviço, a interrupção do serviço será a melhor abordagem.<br/>                                                                                                                                                                                                                                                     |
| [**Desfazer**](control-undo.md)                                   | Restaure a configuração ativa do coletor a partir do arquivo de backup anterior (determinado voltando do carimbo de data/hora original atual). Se a configuração tiver sido definida apenas, isso significa desfazer essa alteração. As chamadas consecutivas serão desfeitas para as configurações anteriores e anteriores. Retorna 1 em caso de êxito, 0 em erro.<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | Valide um texto de configuração para exatidão sem defini-lo como ativo. Retorna 1 em caso de êxito, 0 em erro.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




