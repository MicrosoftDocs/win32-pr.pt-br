---
description: a propriedade MsiLogging define o modo de log padrão para o pacote de Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propriedade MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e166a52e970cdb3e0be5ffae6611a8ea9a299232d55f36a45ba470b3717cafae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042776"
---
# <a name="msilogging-property"></a>Propriedade MsiLogging

a propriedade **MsiLogging** define o modo de log padrão para o pacote de Windows Installer. Se essa propriedade opcional estiver presente na [tabela de propriedades](property-table.md), o instalador gerará um arquivo de log chamado MSI \* . Façam. O caminho completo para o arquivo de log é fornecido pelo valor da propriedade [**MsiLogFileLocation**](msilogfilelocation.md) .

## <a name="value"></a>Valor

O valor dessa propriedade deve ser uma cadeia de caracteres dos caracteres a seguir que especificam o modo de log padrão.



| Valor                                                                        | Significado                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>Encontrei</dt> </dl> | Mensagens de status.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Avisos não fatais.<br/>                                                  |
| <dl> <dt>Oriental</dt> </dl> | Todas as mensagens de erro.<br/>                                                 |
| <dl> <dt>um</dt> </dl> | Inicialização de ações.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Registros específicos da ação.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Solicitações do usuário.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Parâmetros iniciais da interface do usuário.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Informações de saída fatal ou de memória insuficiente.<br/>                            |
| <dl> <dt>o</dt> </dl> | Mensagens de espaço em disco insuficientes.<br/>                                         |
| <dl> <dt>DTI</dt> </dl> | Propriedades do terminal.<br/>                                                |
| <dl> <dt>v</dt> </dl> | Saída detalhada.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Informações adicionais de depuração. disponível somente no Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Libere cada linha para o log.<br/>                                         |



 

## <a name="remarks"></a>Comentários

essa propriedade está disponível a partir do Windows Installer 4,0.

Você não pode usar os valores "+" e " \* " da opção/l no valor da propriedade **MsiLogging** .

O modo de log pode ser definido usando a política, uma opção de linha de comando ou programaticamente. Isso substitui o modo de log padrão. para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte [log Normal](normal-logging.md) na seção [log de Windows Installer](windows-installer-logging.md) .

Se a propriedade **MsiLogging** estiver presente na [tabela de propriedades](property-table.md), o modo de log padrão do pacote poderá ser modificado alterando o valor dessa propriedade usando uma transformação de banco de [dados](database-transforms.md). O modo de log padrão não pode ser alterado usando um [pacote de patch](patch-packages.md) (um arquivo. msp).

Se a propriedade **MsiLogging** tiver sido definida na [tabela de propriedades](property-table.md), o modo de log padrão para todos os usuários do computador poderá ser especificado definindo a política [DisableLoggingFromPackage](disableloggingfrompackage.md) e a política de registro em [log](logging.md) . A configuração da política DisableLoggingFromPackage e da política de log substituirá a propriedade **MsiLogging** para todos os pacotes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




