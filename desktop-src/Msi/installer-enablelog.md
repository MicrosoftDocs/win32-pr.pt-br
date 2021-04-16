---
description: O método EnableLog do objeto instalador habilita o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Método Installer. EnableLog
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
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750000"
---
# <a name="installerenablelog-method"></a>Método Installer. EnableLog

O método **EnableLog** do objeto [**instalador**](installer-object.md) habilita o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.

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

Uma cadeia de caracteres necessária que contém letras que representam os tipos de mensagem a serem registradas. A cadeia de caracteres pode ser uma combinação dos valores a seguir.



| Valor | Descrição                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Mensagens somente de informações.                                                                             |
| w     | Mensagens de aviso não fatais.                                                                            |
| e     | Mensagens de erro que podem ser erros fatais.                                                               |
| f     | Lista de arquivos em uso que precisam ser substituídos.                                                         |
| um     | Início da notificação de ação.                                                                          |
| r     | Registro de dados de ação contendo conteúdo específico à ação.                                              |
| u     | Mensagens de solicitação do usuário.                                                                                 |
| c     | Parâmetros de inicialização da interface do usuário.                                                                          |
| m     | Mensagem de memória insuficiente.                                                                                 |
| v     | O envia grandes quantidades de informações para o arquivo de log, o que geralmente não é útil para os usuários. Pode ser usado para suporte. |
| p     | Despejar tabela de propriedades; "Property = Value" na terminação do mecanismo                                          |
| \+    | Anexar ao arquivo de log existente.                                                                           |
| !     | Libere cada linha para o arquivo de log.                                                                       |
| x     | Informações adicionais de depuração. Essa opção só está disponível com o Windows Server 2003.                      |
| o     | Mensagens de espaço em disco insuficientes.                                                                            |



 

</dd> <dt>

*Restaura* 
</dt> <dd>

Cadeia de caracteres necessária que contém o caminho para o arquivo de log a ser criado. Use uma cadeia de caracteres vazia ("") para desativar o registro em log.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O caminho para o local do arquivo de log já deve existir ao usar esse método. O instalador não cria a estrutura de diretório para o arquivo de log.

As opções de log definidas usando **EnableLog** substituem as configurações de política de registro em log existentes do Windows Installer.

O registro em log substitui um arquivo de log existente por padrão. Você deve usar a letra ' + ' no modo de log para acrescentar a um arquivo de log existente.

A opção '! ' não é recomendada porque pode ter uma instalação significativamente lenta. Essa opção pode ser útil ao depurar uma instalação.

O script de exemplo a seguir ativa o log detalhado para uma instalação. No final da instalação, o arquivo de log gerado estará em c: \\ temp \\ install. log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Log de Windows Installer](windows-installer-logging.md)
</dt> </dl>

 

 




