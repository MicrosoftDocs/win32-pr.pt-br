---
description: As funções de exportação do analisador fornecem toda a funcionalidade dos analisadores na DLL do analisador. Cada DLL do analisador deve implementar ParserAutoInstallInfo e DllMain. As funções de exportação restantes devem ser implementadas para cada analisador incluído na DLL do analisador.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementando funções de exportação do parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e32b3b1aa807a604f058ed8965ef11728f6c12fecb34e27a337682361f8dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778836"
---
# <a name="implementing-parser-export-functions"></a>Implementando funções de exportação do parser

As funções de exportação do analisador fornecem toda a funcionalidade dos analisadores na DLL do analisador. Cada DLL do analisador deve implementar [**ParserAutoInstallInfo**](parserautoinstallinfo.md) e [**DllMain**](dllmain-parser.md). As funções de exportação restantes devem ser implementadas para cada analisador incluído na DLL do analisador.

Os tópicos a seguir mostram como implementar as funções de exportação.



| Termo                                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementando ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Fornece uma descrição e um exemplo de código de implementação da função [**ParserAutoInstallInfo**](parserautoinstallinfo.md) , que identifica os analisadores localizados em uma DLL do analisador.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementando o analisador DllMain](implementing-dllmain-parser.md)<br/>                                    | Fornece uma descrição e um exemplo de código de implementação da função de [**analisador DllMain**](dllmain-parser.md) , que identifica a existência de um analisador e, em seguida, libera recursos que monitor de rede usa para o analisador.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementando o registro](implementing-register.md)<br/>                                                                  | Fornece uma descrição e um exemplo de código de implementação da função [**Register**](register-parser.md) , que registra todas as propriedades de um protocolo.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementando RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Fornece uma descrição e um exemplo de código de implementação da função [**RecognizeFrame**](recognizeframe.md) , que identifica uma instância de um protocolo em um quadro.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementando Anexaproperties](implementing-attachproperties.md)<br/>                          | Fornece uma descrição e um exemplo de código de implementação da função [**attachproperties**](attachproperties.md) , que separa os dados que o analisador reconhece e, em seguida, anexa descrições de propriedade a cada propriedade de protocolo que existe nos dados reconhecidos.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementando Formatproperties](implementing-formatproperties.md)<br/>                          | Fornece uma descrição e um exemplo de código de implementação da função [**formatproperties**](formatproperties.md) , que formata os dados que são exibidos no painel de detalhes da interface do usuário do monitor de rede.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementando cancelamento de registro](implementing-deregister.md)<br/>                                                        | Fornece uma descrição e um exemplo de código de implementação da função de [**cancelamento de registro**](deregister.md) , que libera os recursos usados para registrar Propriedades de protocolo.<br/>                                                                                                     |



 

 

 




