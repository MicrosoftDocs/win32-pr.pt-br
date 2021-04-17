---
description: A propriedade MsiLogging define o modo de log padrão para o pacote de Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propriedade MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782784"
---
# <a name="msilogging-property"></a>Propriedade MsiLogging

A propriedade **MsiLogging** define o modo de log padrão para o pacote de Windows Installer. Se essa propriedade opcional estiver presente na [tabela de propriedades](property-table.md), o instalador gerará um arquivo de log chamado MSI \* . Façam. O caminho completo para o arquivo de log é fornecido pelo valor da propriedade [**MsiLogFileLocation**](msilogfilelocation.md) .

## <a name="value"></a>Valor

O valor dessa propriedade deve ser uma cadeia de caracteres dos caracteres a seguir que especificam o modo de log padrão.



| Valor                                                                        | Significado                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>I</dt> </dl> | Mensagens de status.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Avisos não fatais.<br/>                                                  |
| <dl> <dt>Oriental</dt> </dl> | Todas as mensagens de erro.<br/>                                                 |
| <dl> <dt>um</dt> </dl> | Inicialização de ações.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Registros específicos da ação.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Solicitações do usuário.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Parâmetros iniciais da interface do usuário.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Informações de saída fatal ou de memória insuficiente.<br/>                            |
| <dl> <dt>o</dt> </dl> | Mensagens de espaço em disco insuficientes.<br/>                                         |
| <dl> <dt>DTI</dt> </dl> | Propriedades do terminal.<br/>                                                |
| <dl> <dt>l</dt> </dl> | Saída detalhada.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Informações adicionais de depuração. Disponível somente no Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Libere cada linha para o log.<br/>                                         |



 

## <a name="remarks"></a>Comentários

Essa propriedade está disponível a partir do Windows Installer 4,0.

Você não pode usar os valores "+" e " \* " da opção/l no valor da propriedade **MsiLogging** .

O modo de log pode ser definido usando a política, uma opção de linha de comando ou programaticamente. Isso substitui o modo de log padrão. Para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte [log normal](normal-logging.md) na seção [log de Windows Installer](windows-installer-logging.md) .

Se a propriedade **MsiLogging** estiver presente na [tabela de propriedades](property-table.md), o modo de log padrão do pacote poderá ser modificado alterando o valor dessa propriedade usando uma transformação de banco de [dados](database-transforms.md). O modo de log padrão não pode ser alterado usando um [pacote de patch](patch-packages.md) (um arquivo. msp).

Se a propriedade **MsiLogging** tiver sido definida na [tabela de propriedades](property-table.md), o modo de log padrão para todos os usuários do computador poderá ser especificado definindo a política [DisableLoggingFromPackage](disableloggingfrompackage.md) e a política de registro em [log](logging.md) . A configuração da política DisableLoggingFromPackage e da política de log substituirá a propriedade **MsiLogging** para todos os pacotes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 4,5 no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




