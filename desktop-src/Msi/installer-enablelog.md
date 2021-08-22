---
description: O método EnableLog do objeto Installer permite o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Método Installer.EnableLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 48481a701b7e78de372f5579dab5c9d5976a68063958b0812d6ae1ddc08b109a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631692"
---
# <a name="installerenablelog-method"></a>Método Installer.EnableLog

O **método EnableLog** do objeto [**Installer**](installer-object.md) permite o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*logMode* 
</dt> <dd>

Uma cadeia de caracteres necessária que contém letras que representam os tipos de mensagem a registrar em log. A cadeia de caracteres pode ser uma combinação dos valores a seguir.



| Valor | Descrição                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Mensagens somente informações.                                                                             |
| w     | Mensagens de aviso não fatais.                                                                            |
| e     | Mensagens de erro que podem ser erros fatais.                                                               |
| f     | Lista de arquivos em uso que precisam ser substituídos.                                                         |
| um     | Início da notificação de ação.                                                                          |
| r     | Registro de dados de ação que contém conteúdo específico à ação.                                              |
| u     | Mensagens de solicitação do usuário.                                                                                 |
| c     | Parâmetros de inicialização da interface do usuário.                                                                          |
| m     | Mensagem sem memória.                                                                                 |
| v     | Envia grandes quantidades de informações para o arquivo de log geralmente não útil para os usuários. Pode ser usado para suporte. |
| p     | Tabela de propriedades de despejo; "property = value" na terminação do mecanismo                                          |
| \+    | Anexar ao arquivo de log existente.                                                                           |
| !     | Liberar cada linha para o arquivo de log.                                                                       |
| x     | Informações adicionais de depuração. Essa opção só está disponível com Windows Server 2003.                      |
| o     | Mensagens de espaço fora do disco.                                                                            |



 

</dd> <dt>

*Logfile* 
</dt> <dd>

Cadeia de caracteres necessária que contém o caminho para o arquivo de log a ser criado. Use uma cadeia de caracteres vazia ("") para desativar o registro em log.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O caminho para o local do logfile já deve existir ao usar esse método. O Instalador não cria a estrutura de diretório para o logfile.

As opções de registro em log definidas **usando EnableLog** substituem qualquer configuração Windows política de registro em log do instalador existente.

O registro em log substitui um arquivo de log existente por padrão. Você deve usar a letra '+' no modo de log para anexar a um arquivo de log existente.

A opção '!' não é recomendada porque pode reduzir significativamente a instalação. Essa opção pode ser útil ao depurar uma instalação.

O script de exemplo a seguir liga o log detalhado para uma instalação. No final da instalação, o arquivo de log gerado estará em c: \\ temp \\ install.log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Registro em log do instalador](windows-installer-logging.md)
</dt> </dl>

 

 




